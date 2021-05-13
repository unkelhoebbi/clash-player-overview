<template>
  <div>
    <div class="columns">
      <div class="column">
        <figure class="image">
          <img :src="summary.championAvatar" />
        </figure>
      </div>
    </div>

    <div class="columns" style="text-align: center;">
      <div class="column">
        <h4 class="title is-4">Games</h4>
        <h4 class="subtitle is-4">{{ summary.games }}</h4>
      </div>

      <div class="column">
        <h4 class="title is-4">KDA</h4>
        <h4 class="subtitle is-4">
          {{ ((summary.kills + summary.deaths) / summary.deaths).toFixed(2) }}
        </h4>
      </div>

      <div class="column">
        <h4 class="title is-4">Win</h4>
        <h4 class="subtitle is-4">{{ summary.winrate }}%</h4>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import { ChampionSummary } from './SummonerOverviewSample.vue';

export default defineComponent({
  name: 'ChampionStats',
  props: {
    summary: {
      type: Object as PropType<ChampionSummary>,
      required: true,
    },
  },
});
</script>
