<template>
  <div class="wrapper">
    <section class="container" v-if="countries">
      <countryCard v-for="country of countries"
      :key="country.id"
      :country="country" 
      />
    </section>
  </div>

</template>

<script>
import axios from 'axios';
import countryCard from '../components/countryCard.vue';

export default {
  name: 'HomePage',
  components: {
    countryCard
  },
  head: () => {
    return {
      title: "Travel Buddy in Nuxt",
      meta: [
        {
          charset: "utf-8"
        },
        {
          name: "viewport",
          content: "width=device-width, initial-scale=1"
        },
        {
          hid: "description",
          name: "description",
          content: "Helping you find the right place to travel to"
        }
      ]
    }
  },
  data() {
    return {
      loading: true,
      countries: null,
      errored: false,
    }
  },
  mounted () {
    axios
      .get('https://restcountries.com/v3.1/all')
      .then(response => (this.countries = response.data))
      .catch(error => {
        console.log(error)
        this.errored = true
      })
      .finally(() => this.loading = false)
  },
}
</script>

<style>
.container {
  min-height: 100vh;
  max-width: 1200px;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  text-align: center;
  flex-wrap: wrap;
}

.heading {
  text-align: center;
  font-size: 2rem;
  color: #555555;
  margin: 2rem auto;
}

img {
  max-width: 150px;
}

.title {
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  display: block;
}
</style>