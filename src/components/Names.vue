<template>
  <div>
    <h2>{{ title }}</h2>
    {{ name }} <br/>
    {{ nameIsGreat }} <br/>
    <input
    v-model="name"
    />
  </div>
</template>

<script>
export default {
  props: ['title'],
name: 'Names',
data: () => ({
  name: "foo"
}),
computed: {
  nameIsGreat() {
    return this.name + " is great"
  }
}

};
</script>

<style scoped></style>
