<template>
  <div>
    <h2>My Title</h2>
    {{ names }}
<ul>
  <li
  v-for="name in names"
  :key="name"
  >
  {{name}}
  </li>
</ul>
    <input
    v-model="name"
    />
<button
v-show="name.length > 0"
v-on:click="onClick"
>
  Add
</button>

  </div>
</template>

<script>
export default {
name: 'Names',
data: () => ({
  name: "",
}),
computed: {
  names() {
    return this.$store.state.names;
  }
},
methods: {
  onClick() {
    this.$store.dispatch('slowAddName', this.name);
  }
}

};
</script>

<style scoped></style>
