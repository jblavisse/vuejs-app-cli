<template>
    <div class="fuck">
        <input type="text" placeholder="Your color!" v-model="colorInput">
        <button @click="changeTitleColor" >OK</button>
        <h2 :class="classTitle">Change my fucking color, bitch!</h2>
    </div>
</template>

<script>
export default {
    name: 'Fuck',
    data: function() {
        return {
            classTitle: "title",
            colorInput: ""
        }
    },
    methods: {
        changeTitleColor: function() {
            if(['red', 'blue', 'green'].includes(this.colorInput))
            {
                this.classTitle = `title title--${this.colorInput}`;
            }    
            else {
                this.classTitle = "title";
            }    
        }
    }
}
</script>

<style lang="scss">
.title {
    font-size: 48px;
    color: black;

    &--red {
        color: red;
    }

    &--green {
        color: green;
    }

    &--blue {
        color: blue;
    }
}
</style>