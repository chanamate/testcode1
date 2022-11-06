<template>
  <h1 class="text-center">Header</h1>
  <div class="flex">
    <div class="card">
      <h2>Card1</h2>
      <p>description</p>
      <input type="text" v-model="input" />
      <button @click="changeInput">Change Input</button>
    </div>
    <h3>{{ `Name: ${selectedPerson.name} Age: ${selectedPerson.age}` }}</h3>
    <h3>{{ "Name: " + selectedPerson.name + " " + selectedPerson.age }}</h3>
    <h3>Name: {{ selectedPerson.name }} Age: {{ selectedPerson.age }}</h3>
    <div v-for="(item, index) in person" :key="index" class="card">
      <h2>Card2</h2>
      <p>description</p>
      <h3>Name: {{ item.name }}</h3>
      <h3>Age: {{ item.age }}</h3>
      <button @click="changeInput2(item)">Change Input</button>
    </div>

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
  components: [Card],
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
    };
  },

  methods: {
    changeInput() {
      this.currentText = this.input;
    },
    changeInput2(person) {
      console.log("person: ", person);
      console.log("berfore: ", this.selectedPerson);
      this.selectedPerson = person;
      console.log("after: ", this.selectedPerson);
      console.log("...array", [...this.person, ...this.person])
      let object = {...this.selectedPerson, hair: "black"}
      console.log("...object", object)
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

.f_frame,
.f_frame * {
  box-sizing: border-box;
}
.f_frame {
  background: #f3f3f3;
  width: 1600px;
  height: 1000px;
  position: relative;
  overflow: hidden;
}
.iconsax-linear-more {
  position: absolute;
  left: 9px;
  top: 10px;
  overflow: visible;
}
.model {
  background: #d9d9d9;
  border-radius: 20px;
  width: 1489px;
  height: 426px;
  position: absolute;
  left: 55px;
  top: 545px;
}
.title_dt {
  width: 233.82px;
  height: 47.31px;
  position: static;
}
.back_dt {
  background: #d9d9d9;
  border-radius: 20px;
  width: 233.82px;
  height: 47.31px;
  position: absolute;
  left: 315.49px;
  top: 476.25px;
}
.dt {
  color: #000000;
  text-align: center;
  font: 400 16px "Inter";
  position: absolute;
  left: 315.49px;
  top: 476.25px;
  width: 233.82px;
  height: 47.31px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.title_ng {
  width: 233.82px;
  height: 47.31px;
  position: static;
}
.back_ng {
  background: #d9d9d9;
  border-radius: 20px;
  width: 233.82px;
  height: 47.31px;
  position: absolute;
  left: 55px;
  top: 476.25px;
}
.failure {
  color: #000000;
  text-align: center;
  font: 400 16px "Inter";
  position: absolute;
  left: 55px;
  top: 476.25px;
  width: 233.82px;
  height: 47.31px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.line-1 {
  border: solid #000000;
  border-width: 3px 0 0 0;
  width: 1600px;
  height: 0px;
  position: absolute;
  left: 0px;
  top: 78px;
  transform-origin: 0 0;
  transform: rotate(0deg) scale(1, 1);
}
.line-2 {
  border: solid #000000;
  border-width: 1px 0 0 0;
  width: 1455px;
  height: 0px;
  position: absolute;
  left: 67px;
  top: 444px;
}
.model2 {
  width: 596px;
  height: 295px;
  position: static;
}
.back_model {
  background: #d9d9d9;
  border-radius: 20px;
  width: 596px;
  height: 295px;
  position: absolute;
  left: 55px;
  top: 110px;
}
.modef03 {
  width: 477px;
  height: 46px;
  position: static;
}
.back_model2 {
  background: #c5c5c5;
  border-radius: 5px;
  width: 477px;
  height: 46px;
  position: absolute;
  left: 129px;
  top: 312px;
  box-shadow: 2px 4px 4px 0px rgba(0, 0, 0, 0.25);
}
.model-f03 {
  color: #000000;
  text-align: center;
  font: 400 20px "Inter";
  position: absolute;
  left: 129px;
  top: 312px;
  width: 477px;
  height: 46px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.modef02 {
  width: 477px;
  height: 46px;
  position: static;
}
.back_model3 {
  background: #c5c5c5;
  border-radius: 5px;
  width: 477px;
  height: 46px;
  position: absolute;
  left: 129px;
  top: 245px;
  box-shadow: 2px 4px 4px 0px rgba(0, 0, 0, 0.25);
}
.model-f02 {
  color: #000000;
  text-align: center;
  font: 400 20px "Inter";
  position: absolute;
  left: 129px;
  top: 245px;
  width: 477px;
  height: 46px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.modef01 {
  width: 477px;
  height: 46px;
  position: static;
}
.back_model4 {
  background: #c5c5c5;
  border-radius: 5px;
  width: 477px;
  height: 46px;
  position: absolute;
  left: 129px;
  top: 178px;
  box-shadow: 2px 4px 4px 0px rgba(0, 0, 0, 0.25);
}
.model-f01 {
  color: #000000;
  text-align: center;
  font: 400 20px "Inter";
  position: absolute;
  left: 129px;
  top: 178px;
  width: 477px;
  height: 46px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.model-- {
  color: #000000;
  text-align: left;
  font: 400 24px "Inter";
  position: absolute;
  left: 80px;
  top: 110px;
  width: 571px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
.summary_employee_id {
  background: #d9d9d9;
  border-radius: 20px;
  width: 781px;
  height: 137px;
  position: absolute;
  left: 763px;
  top: 268px;
}
.fabrication-f-frame {
  color: #000000;
  text-align: center;
  font: 400 48px "Inter";
  position: absolute;
  left: 0px;
  top: 10px;
  width: 1600px;
  height: 100px;
}
.employee_id {
  background: #d9d9d9;
  border-radius: 20px;
  width: 781px;
  height: 137px;
  position: absolute;
  right: 56px;
  top: 110px;
}
</style>
