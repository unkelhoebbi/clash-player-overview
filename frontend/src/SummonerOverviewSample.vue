<template>
  <div>
    <Form v-bind:name="name" />
    <div v-for="summary in games" :key="summary.championName">
      <ChampionStats v-bind:summary="summary" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ChampionStats from './ChampionStats.vue';
import Form from './Form.vue';

export interface ChampionSummary {
  assists: number;
  championAvatar?: string;
  championName: string;
  deaths: number;
  games: number;
  kills: number;
  winrate: number;
}

interface State {
  games: ChampionSummary[];
  name: string;
}

export default defineComponent({
  name: 'SummonerOverviewSample',
  components: {
    ChampionStats, Form,
  },

  data: (): State => ({
    games: [
      {
        assists: 7.6,
        championAvatar:
          'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/LeeSin_0.jpg',
        championName: 'Lee Sin',
        deaths: 7.7,
        games: 16,
        kills: 5.8,
        winrate: 56,
      },
      {
        assists: 12.0,
        championAvatar:
          'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Ivern_0.jpg',
        championName: 'Ivern',
        deaths: 5.3,
        games: 12,
        kills: 2.3,
        winrate: 58,
      },
      {
        assists: 5.2,
        championAvatar:
          'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Samira_0.jpg',
        championName: 'Samira',
        deaths: 5.5,
        games: 15,
        kills: 8.3,
        winrate: 67,
      },
      {
        assists: 7.3,
        championAvatar:
          'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Kayn_0.jpg',
        championName: 'Kayn',
        deaths: 7.0,
        games: 12,
        kills: 7.1,
        winrate: 42,
      },
    ],
    name: '',
  }),
});
</script>
