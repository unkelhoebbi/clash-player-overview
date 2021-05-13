<template>
  <div class="columns is-vcentered">
    <div class="column">
      <label class="label">Name</label>
      <div class="control">
        <input v-bind="name" class="input" type="text" placeholder="Enter summoner name .." />
      </div>
    </div>
    <div class="column is-one-third" style="margin-top: auto;">
      <button class="button is-primary">Send</button>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Form',
  props: {
    name: String,
  },
});
</script>
