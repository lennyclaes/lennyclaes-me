<template>
  <div class="home" :class="'home-'+background">
    <h1 class="heading">Working on the future</h1>
    <h2 class="tagline">Hold on</h2>
    <loader />
  </div>
</template>

<script>
import loader from '../components/userFeedback/loader.vue';
// @ is an alias to /src

export default {
  name: "Home",
  components: {
    loader
  },
  data: () => {
    return {
      background: Math.floor(Math.random() * 4) + 1
    }
  }
};
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100vh;

  &-1 {
    background: #c44a4a;
  }
  &-2 {
    background: #71c44a;
  }
  &-3 {
    background: #4a8dc4;
  }
  &-4 {
    background: #c44aaa;
  }
}

.heading {
  font-size: 72px;
  font-family: "Catamaran", Arial, Helvetica, sans-serif;
  text-align: center;
}

.tagline {
  font-size: 32px;
  font-family: "Catamaran", Arial, Helvetica, sans-serif;
  text-align: center;
}
</style>