<script setup>
import Layout from '../../Layouts/AppLayout.vue'
import { Head } from '@inertiajs/vue3'
import Create from './Create.vue'

defineProps({ posts: Array })
// console.log('Hersoo', posts);
</script>

<template >
  <Layout>
    <div class="container mx-auto">
         <!-- <Head title="Welcome" /> -->
        <h1>Posts</h1>
        <p>Hello {{ posts.name }}, welcome to your first Inertia app!</p>
        <Create />
    </div>
  </Layout>
</template>bn