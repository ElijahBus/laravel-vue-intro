<template>
    <div class>
        <br />
        <GradeButton text="Subscribe" :action="subscribe" />
    </div>
</template>

<script>
import GradeButton from "./GradeButton.vue";
export default {
    components: { GradeButton },
    methods: {
        subscribe() {
            alert("Thank you for subscribing..");
        }
    },
    mounted() {
        console.log("Component mounted.");
    },
}
</script>
