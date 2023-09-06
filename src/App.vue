<script setup>
import HelloWorld from './components/HelloWorld.vue';
import { h, ref } from 'vue';
import { renderToString } from 'vue/server-renderer';

const html = ref('');

const htmlFunc = async () => {
  const mycomp = h(HelloWorld, { name: 'Dale', phone: '777', cell: '111' });
  const rendered = await renderToString(mycomp);
  html.value = rendered.replace('<!--[-->', '').replace('<!--]-->', '');
};
</script>

<template>
  <div>
    <button :onClick="htmlFunc">Get</button>
    <p>bob</p>
    <p v-html="html"></p>
  </div>
</template>
