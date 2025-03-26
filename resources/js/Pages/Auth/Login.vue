<template>
    Enter Credentials
    <form @submit.prevent="submit">
        <input type="email" placeholder="email" v-model="form.email">
        <input type="password" placeholder="password" v-model="form.password">
        <button type="submit">Submit</button>
    </form>

</template>

<script setup>

import { useForm } from '@inertiajs/vue3';

const form = useForm({
email : '',
password : '',
})


const submit = () => {
    form.post('/authenticate')
}

</script>