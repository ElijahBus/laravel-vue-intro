<template>
    <div class="person-grades__wrapper">
        <h2>Robert's grades</h2>
        <hr />

        <div class="person-card">
            <div class="person-card__header">
                <!-- <img src alt=" " /> -->
            </div>

            <div class="person-card__description">
                <h4 class="bg-danger text-light">Grades: {{ grade }}</h4>

                <grade-button :text="upgradeBtnText" :action="upgrade" />
                <grade-button text="Downgrade" :action="downgrade" />
            </div>
        </div>
    </div>
</template>

<script>
import GradeButton from "./GradeButton.vue";

export default {
    name: "Person",
    components: { GradeButton },
    data: () => {
        return {
            grade: 0,
            upgradeBtnText: "Upgrade"
        }
    },
    methods: {
        upgrade() {
            this.grade = 5;
        },

        downgrade() {
            this.grade -= 3;
        }
    },
    mounted() {
        // Fetching the grades
        this.grade = 8;
    }
}

</script>
