<template>
  <h1 class="text-center">Header</h1>
  <div class="flex">
    <div class="card">
      <h2>Card1</h2>
      <p>description</p>
      <v-text-field
        variant="underlined"
        label="LABEL"
        type="text"
        v-model="input"
      />
      <v-btn @click="changeInput"
        ><v-icon>mdi-checkbox-multiple-blank</v-icon><v-icon>mdi-pencil</v-icon>Change Input</v-btn
      >
    </div>
    <!-- <Card :items="person" /> -->
    <v-card theme="dark" class="mx-auto" width="400" prepend-icon="mdi-home">
      <template v-slot:title> This is a title </template>
      <v-card-text> This is content </v-card-text>
    </v-card>
    <v-table theme="dark">
      <thead>
        <tr>
          <th class="text-left">Name</th>
          <th class="text-left">Calories</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in person" :key="item.name">
          <td>{{ item.name }}</td>
          <td>{{ item.age }}</td>
        </tr>
      </tbody>
    </v-table>
    <!-- <h3>{{ `Name: ${selectedPerson.name} Age: ${selectedPerson.age}` }}</h3>
    <h3>{{ "Name: " + selectedPerson.name + " " + selectedPerson.age }}</h3>
    <h3>Name: {{ selectedPerson.name }} Age: {{ selectedPerson.age }}</h3>
    <div v-for="(item, index) in person" :key="index" class="card">
      <h2>Card2</h2>
      <p>description</p>
      <h3>Name: {{ item.name }}</h3>
      <h3>Age: {{ item.age }}</h3>
      <button @click="changeInput2(item)">Change Input</button>
    </div> -->

    <!-- <div class="card">
      <h2>Card2</h2>
      <p>description</p>
      <h3>{{ currentText }}</h3>
    </div>
    <div class="card">
      <h2>Card3</h2>
      <p>description</p>
      <h3>{{ currentText }}</h3>
    </div> -->
  </div>
</template>

<script>
import Card from "./components/Card";

export default {
  name: "App",
  components: { Card },
  data() {
    return {
      input: "",
      currentText: "123",
      array: ["123", "456"],
      selectedPerson: { name: "default", age: 99 },
      person: [
        {
          name: "John",
          age: 23,
        },
        {
          name: "Mary",
          age: 11,
        },
        {
          name: "Peter",
          age: 12,
        },
      ],
      desserts: [
        {
          name: "Frozen Yogurt",
          calories: 159,
        },
        {
          name: "Ice cream sandwich",
          calories: 237,
        },
        {
          name: "Eclair",
          calories: 262,
        },
        {
          name: "Cupcake",
          calories: 305,
        },
        {
          name: "Gingerbread",
          calories: 356,
        },
        {
          name: "Jelly bean",
          calories: 375,
        },
        {
          name: "Lollipop",
          calories: 392,
        },
        {
          name: "Honeycomb",
          calories: 408,
        },
        {
          name: "Donut",
          calories: 452,
        },
        {
          name: "KitKat",
          calories: 518,
        },
      ],
    };
  },
  name: "App",

  methods: {
    changeInput() {
      this.currentText = this.input;
    },
    changeInput2(person) {
      console.log("person: ", person);
      console.log("berfore: ", this.selectedPerson);
      this.selectedPerson = person;
      console.log("after: ", this.selectedPerson);
      console.log("...array", [...this.person, ...this.person]);
      let object = { ...this.selectedPerson, hair: "black" };
      console.log("...object", object);
    },
  },
};
</script>

<style>
.flex {
  display: flex;
  flex-direction: column;

  justify-content: center;
  align-items: center;

  gap: 4rem;
  border: 3px solid salmon;
}
.card {
  background-color: white;
  border: 3px solid #3c3c3c;
  border-radius: 15px;
  padding: 2rem 4rem;
}
.text-center {
  text-align: center;
}
</style>
