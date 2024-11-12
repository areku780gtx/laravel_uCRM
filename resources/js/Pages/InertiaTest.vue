<script setup>
import { Link } from "@inertiajs/inertia-vue3";
import { ref } from "vue";
const newTitle = ref("");
const newContent = ref("");
</script>

<template>
    <h1>InertiaTest</h1>
    <a href="/">a タグ経由です </a>
    <Link href="/">Link 経由です</Link>
    <Link :href="route('inertia.index')">名前付きルートの確認です</Link><br />
    <Link :href="route('inertia.show', { id: 50 })"
        >名前付きルートの確認です</Link
    ><br />
    <input type="text" name="newTitle" v-model="newTitle" />
    <input type="text" name="newContent" v-model="newContent" />
    <Link
        as="button"
        method="post"
        :href="route('inertia.store')"
        :data="{ title: newTitle, content: newContent }"
    >
        作成
    </Link>
</template>
