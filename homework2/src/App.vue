<template>
  <h1 v-if="age < 4">Малыш</h1>
  <h1 v-else-if="age > 3 & age < 13">Ребёнок</h1>
  <h1 v-else-if="age < 19 & age > 12">Подросток</h1>
  <h1 v-else-if="age > 18 & age < 26">Взрослый</h1>
  <h1 v-else-if="age > 25 & age < 76">Старик</h1>
  <h1 v-else>Призрак</h1>
  <button @click="askage">Ответить на вопрос</button>

</template>

<script>
export default {
  methods: {
    askage() {
      this.age = prompt("Сколько вам лет?")
    }
  },
  computed: {

  },
  data() {
    return {
      age: "",
    }
  },
}
</script>

<style></style>
