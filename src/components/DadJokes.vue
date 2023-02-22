<template>
  <div class="card w-50 h-50 py-3 px-3" style="width: 18rem">
    <div
      class="card-body d-flex flex-column justify-content-between align-items-end"
    >
      <h2 class="card-title">{{ setup }}</h2>
      <h5 v-if="punchline !== ''" class="card-text fw-bold">
        {{ punchline }} 😂
      </h5>
      <btn class="btn btn-danger btn-lg" @click="getDadJokes">Reload 💫</btn>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'DadJokes',
  data() {
    return {
      setup: '',
      punchline: '',
    };
  },
  mounted() {
    this.getDadJokes();
  },
  methods: {
    async getDadJokes() {
      try {
        let data = await axios({
          url: 'https://official-joke-api.appspot.com/jokes/random',
          method: 'GET',
        });
        const jokes = data.data;
        this.setup = jokes.setup;
        this.punchline = jokes.punchline;
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.card-body {
  text-align: right !important;
}

.card-title {
  font-weight: 400 !important;
}

//.card-text {
//  font-weight: 600 !important;
//}

.btn {
  width: 140px !important;
}
</style>
