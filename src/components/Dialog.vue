<template>
<div>
    <div
    class="dialog"
    v-if="shown">
    <slot />
    </div>
    </div>
</template>

<script>
export default {
     data: () => ({
         shown: false,
     }),
     methods: {
         show() {
             this.shown = true;
         },
         hide() {
             this.shown = false;
         },
     }
}
</script>

<style>
.dialog {
    border: 1px solid black;
    background: #eee;
    border-radius: 1em;
    padding: 2em;
    margin: 1em;
}
</style>