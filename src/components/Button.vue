<template>
    <button :class="classname"
        @click="incrementCount">Cliqué {{count}} fois</button>
</template>

<script>
export default {
    name: 'Button',
    data: function() {
        return {
            count: 0,
            classname: "button"
        }
    },
    methods: {
        incrementCount: function() {
            this.count++;
            this.classname = "button button--red"
        }
    }
}
</script>

<style lang="scss">
.button {
    padding: 20px;
    color: white;
    background-color: blue;

    &--red {
        background-color: red;
    }
}
</style>