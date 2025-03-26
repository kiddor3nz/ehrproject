<template>
    <Frontend>
        <div>
            <h1>Welcome, {{ $page.props.auth.user?.name }}</h1>
            <p>Email: {{ $page.props.auth.user?.email }}</p>

            <button @click.prevent="logout">Logout</button>
        </div>
    </Frontend>
</template>

<script setup>
import { router } from '@inertiajs/vue3';
import Frontend from '@/Layouts/FrontendLayout.vue';

const logout = () => {
    router.post('/logout');
};
</script>
