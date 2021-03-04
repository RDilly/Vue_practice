<template>
  <div>
    <h2>{{ title }}</h2>
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
  props: ['title'],
name: 'Names',
data: () => ({
  name: "",
  names: [ 
    "Sophie",
    "Sadie"
  ]
}),
watch: {
  names(val) {
    console.log(val)
  }
},
methods: {
  onClick() {
    this.names.push(this.name);
  }
}

};
</script>

<style scoped></style>
