<template>
  <div>
    <label class="label">Name</label>
    <div class="control">
      <input v-model="name" class="input" type="text" placeholder="Enter summoner name .." />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'SummonerOverview',
  state: {
    name: '',
  },
});
</script>
