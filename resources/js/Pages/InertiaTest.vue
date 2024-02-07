<script setup>
import { Link } from '@inertiajs/vue3';
import { ref } from 'vue';

const newTitle = ref('');
const newContent =ref('');

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

  <div class="mb-8"></div>

  <input type="text" name="newTitle" v-model="newTitle">{{ newTitle }}<br>
  <input type="text" name="newContent" v-model="newContent">{{ newContent }}<br>

  <Link as="button" :href="route('inertia.store')" method="post"
  :data="{
    title: newTitle,
    content: newContent,
  }">
    DB保存テスト
  </Link>
</template>
