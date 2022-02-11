<template>
    <button @click="action">{{ text }}</button>
</template>

<script>
export default {
    name: "GradeButton",
    props: {
        text: { type: String, required: true },
        action: Function
    }
}

</script>

<style scoped>
button {
    background-color: #fff;
    border: 1px solid black;
    border: 10px;
    color: black;
}
</style>
