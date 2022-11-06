<template>
  <h1 class="text-center">Card Component</h1>
  <div class="flex">
    <div v-for="(item, index) in items" :key="index" class="card">
      <h2>Card2</h2>
      <p>description</p>
      <h3>Name: {{ items.name }}</h3>
      <h3>Age: {{ items.age }}</h3>
      <!-- <button @click="changeInput2(item)">Change Input</button> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["items"],
  data() {
    return {};
  },
  methods: {},

  created(){
    console.log(this.items)
  }
};
</script>

<style></style>
