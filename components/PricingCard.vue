<template>
    <div style="width:100%;">
      <b-card-group deck>
        <b-col cols="12" lg="4">
          <pricing-card-free
            v-for="item in pricingOptionsFree"
            v-bind:item="item"
            v-bind:key="item.id"
            v-bind:name="item.name"
            v-bind:cost="item.cost"
            v-bind:feature1="item.features[0]"
            v-bind:feature2="item.features[1]"
            v-bind:feature3="item.features[2]"
            v-bind:feature4="item.features[3]"
            v-bind:cta="item.cta"
          ></pricing-card-free>
        </b-col>
        <b-col cols="12" lg="4">
          <pricing-card-pro
            v-for="item in pricingOptionsPro"
            v-bind:item="item"
            v-bind:key="item.id"
            v-bind:name="item.name"
            v-bind:cost="item.cost"
            v-bind:feature1="item.features[0]"
            v-bind:feature2="item.features[1]"
            v-bind:feature3="item.features[2]"
            v-bind:feature4="item.features[3]"
            v-bind:cta="item.cta"
          ></pricing-card-pro>
        </b-col>
        <b-col cols="12" lg="4">
          <pricing-card-enterpsie
            v-for="item in pricingOptionsEnterprise"
            v-bind:item="item"
            v-bind:key="item.id"
            v-bind:name="item.name"
            v-bind:cost="item.cost"
            v-bind:feature1="item.features[0]"
            v-bind:feature2="item.features[1]"
            v-bind:feature3="item.features[2]"
            v-bind:feature4="item.features[3]"
            v-bind:cta="item.cta"
          ></pricing-card-enterpsie>
        </b-col>
      </b-card-group> 

      <b-modal id="plan-modal" title="New Plan Selected">
        <p class="my-4">You have chosen: <b>{{chosenPlan}}</b></p>
      </b-modal>
    </div>
</template>

<script>
import PricingCardFree from './PricingCardFree.vue';
import PricingCardPro from './PricingCardPro.vue';
import PricingCardEnterpsie from './PricingCardEnterprise.vue';

export default {
  components: { PricingCardFree, PricingCardPro, PricingCardEnterpsie },
  name: 'PricingCard',
  props: {},
  computed: {
    pricingOptionsFree () {
      return this.$store.state.pricingOptions.filter( i => i.name == "Free" );
    },
    pricingOptionsPro () {
      return this.$store.state.pricingOptions.filter( i => i.name == "Pro" );
    },
    pricingOptionsEnterprise () {
      return this.$store.state.pricingOptions.filter( i => i.name == "Enterprise" );
    },
    chosenPlan () {
      return this.$store.state.chosenPlan
    }
  },
  methods: {},
};
</script>