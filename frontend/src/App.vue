<template>
  <div class="columns vertical-center">
    <SummonerOverview class="column" />
    <SummonerOverview class="column" />
    <SummonerOverview class="column" />
    <SummonerOverview class="column" />
    <SummonerOverviewSample class="column" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import '../node_modules/bulma/css/bulma.css';
import SummonerOverview from './SummonerOverview.vue';
import SummonerOverviewSample from './SummonerOverviewSample.vue';

export default defineComponent({
  name: 'App',
  components: { SummonerOverview, SummonerOverviewSample },
});
</script>
