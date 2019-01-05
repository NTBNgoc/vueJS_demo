<template>
    <div class="my-component">
        <div>{{ message.type }}</div>
        <div>{{ message.text }}</div>
        <div><button @click="changeMessage">Click me</button></div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: {
                type: 'hello',
                text: 'How are you?'
            }
        }
    },
    methods: {
        changeMessage() {
            this.message.type = 'hi'
            this.message.text = 'I am fire thanks'
        }
    },
    watch: {
        message: {
            handler: function () {
                console.log('something changed')
            },
            deep: true
        }
    }
}
</script>

<style lang="scss" scoped>
    .my-component {
        color: red;
    }
</style>
