<script setup>
import MYVueComponent from "../components/MYVueComponent.vue";
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h1>First test on vue</h1>
    <MYVueComponent name="World" />
    <input type="text" v-model="content" />
    <button class="button" @click="decreaseCount()">decrease</button>
    <span>{{ count }}</span>
    <button class="button" @click="increaseCount()">increase</button>
    <button class="button" @click="save()">SAVE</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      content: "",
    };
  },
  methods: {
    decreaseCount() {
      this.count--;
    },
    increaseCount() {
      this.count++;
    },
    save() {
      if (!this.content) {
        alert("please fill!");
      }
      console.log(this.content);
    },
  },
};
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: block;
    align-items: center;
  }
  .button {
    padding: 0.5rem 1rem;
    margin-left: 1rem;
  }
}
</style>
