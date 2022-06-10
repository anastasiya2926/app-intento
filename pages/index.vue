<template>
  <div class="index">
    <!-- header -->
    <GlobalHeader />

    <!-- banner -->
    <HomeBanner />

    <!-- reccomendations -->
    <HomeRecommendations>
      <CardTypeA
        v-for="(card, i) in rec" :key="i"
        :title="card.title"
        :text="card.text"
        :picture="card.picture"
        buttonContent="clicka aquí"
      />

    </HomeRecommendations>

    <!-- news -->

    <!-- keepListening -->

    <!-- footer -->
    <GlobalFooter />
  </div>
</template>

<script>
import CardTypeA from "~/components/Cards/CardTypeA.vue";
import {mapState} from "vuex"
export default {
    name: "IndexPage",
    components: { CardTypeA }, 
    computed: {
      ...mapState({
        rec: state => state.home.recommendations
      })
    }
};
</script>
