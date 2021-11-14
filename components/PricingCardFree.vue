<template>
  <b-card :title="'$' + cost + '/mo'" header-tag="header" class="pricing-card">
    <template #header>
      <h4 class="mb-0">{{name}}</h4>
    </template>
    <b-card-text>{{feature1}}</b-card-text>
    <b-card-text>{{feature2}}</b-card-text>
    <b-card-text>{{feature3}}</b-card-text>
    <b-card-text>{{feature4}}</b-card-text>
    <b-button v-b-modal.plan-modal variant="outline-primary" v-on:click="changePlan">{{cta}}</b-button>
  </b-card>
</template>

<script>
export default {
  name: 'PricingCardFree',
  props: {
    name: String,
    cost: Number,
    feature1: String,
    feature2: String,
    feature3: String,
    feature4: String,
    cta: String
  },
  computed: {},
  methods: {
    changePlan() {
      this.$store.commit('chosenPlanFree')
      console.log(this.$store.state.chosenPlan)
    }
  },
};
</script>