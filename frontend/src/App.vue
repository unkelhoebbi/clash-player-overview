<template>
  <section class="section">
    <div class="container">
      <h1 class="title">Hello World</h1>
      <p class="subtitle">
        My first website with
        <strong>Bulma</strong>!
      </p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import '../node_modules/bulma/css/bulma.css';

export default defineComponent({
  name: 'App',
});
</script>
