<template>
    <div class="card m-5 p-5">
        <h4>Hello , {{ fullName }}</h4>

        <input
            type="text"
            name="first-name"
            v-model="firstName"
            class="form-control my-1"
            placeholder="Firstname"
        />

        <input
            type="text"
            name="last-name"
            v-model="lastName"
            class="form-control my-1"
            placeholder="Lastname"
        />

        <select name="school" v-model="school" class="form-control my-1">
            <option value>-- Select school ---</option>
            <option value="KIST">KIST</option>
            <option value="ULK">ULK</option>
            <option value="UR">UR</option>
        </select>

        <button
            type="submit"
            id="submit-user-profile"
            class="btn btn-primary"
            @click="submitUserProfile()"
        >Submit</button>
    </div>
</template>

<script>
import axios from "axios"

export default {
    name: 'Greetings',
    data() {
        return {
            firstName: '',
            lastName: '',
            fullName: '',
            school: ''
        }
    },
    methods: {
        submitUserProfile() {

            // axios.post('/usr', data)
            this.fullName = this.firstName + ' ' + this.lastName;
            console.log(`Data submitted successfully: ${this.firstName} - ${this.lastName} - ${this.school}`)
        }
    }
}
</script>

<style>
</style>
