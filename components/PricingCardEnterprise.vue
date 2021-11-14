<template>
  <b-card :title="'$' + cost + '/mo'" header-tag="header" border-variant="primary" header="Primary" header-bg-variant="primary" header-text-variant="white" class="pricing-card">
    <template #header>
      <h4 class="mb-0">{{name}}</h4>
    </template>
    <b-card-text>{{feature1}}</b-card-text>
    <b-card-text>{{feature2}}</b-card-text>
    <b-card-text>{{feature3}}</b-card-text>
    <b-card-text>{{feature4}}</b-card-text>
    <b-button v-b-modal.plan-modal variant="primary" v-on:click="changePlan">{{cta}}</b-button>
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
      this.$store.commit('chosenPlanEnterprise')
      console.log(this.$store.state.chosenPlan)
    }
  },
};
</script>