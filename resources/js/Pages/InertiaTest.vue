<script setup>
import { Link } from '@inertiajs/vue3';
</script>

<template>
  Inertiaテストです。<br>

  <a href="/">aタグから</a>
  <br>

  <Link href="/">Linkコンポーネントから</Link>
  <br>

  <Link :href="route('inertia.index')">ルートの確認です</Link>
  <br>

  <Link :href="route('inertia.show', { id: 50 })">showルートです</Link>
  <br>
</template>
