<template>
    <div>
        <p>{{ message }}</p>
        <button v-on:click="reverseMessage">
            Reverse
        </button>
        <!-- <p>{{ reverseMessage }}</p> -->
        <p>Counter: {{ counter }}</p>

        <!-- <ul>
        <todo-item
            v-for="item in groceryList"
            v-bind:todo="item"
            v-bind:key="item.id"
        ></todo-item>
        </ul> -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: "PhilBest",
            blah: "nyaha",
            counter: 0,
            groceryList: [
                { id: 1, text: 'Javascript'},
                { id: 2, text: 'React'},
                { id: 3, text: 'Vue'},
                { id: 4, text: 'Blazor'},
            ]
        }
    },
    methods: {
        reverseMessage() {
            this.message = this.message
            .split('')
            .reverse()
            .join('')
        }
    },
    mounted() {
        setInterval(() => {
            this.counter++
        }, 1000)
    }          
}
</script>

<style>
    #app_div {
        font-family: Helvetica, Arial, sans-serif;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
