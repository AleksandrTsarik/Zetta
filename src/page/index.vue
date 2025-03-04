<template>
  <section class="section">
    <Banner />
  </section>
  <section class="section">
    <Offer />
  </section>
  <section class="section">
    <Taxi />
  </section>
  <section class="section">
    <Payments />
  </section>
  <section class="section">
    <Refund />
  </section>
  <section class="section">
    <Insured />
  </section>
  <section class="section">
    <Document />
  </section>
  <section class="section">
    <Service />
  </section>
</template>
<script>
import Banner from '@/components/TheBanner.vue';
import Offer from '@/components/TheOffer.vue';
import Taxi from '@/components/TheTaxi.vue';
import Payments from '@/components/ThePayments.vue';
import Refund from '@/components/TheRefund.vue';
//import Zetta from '@/components/TheZetta.vue';
import Service from '@/components/TheService.vue';
import Document from '@/components/TheDocument.vue';
import Insured from '@/components/TheInsured.vue';
export default {
  components: {
    Banner,
    Offer,
    Taxi,
    Payments,
    Refund,
    //Zetta,
    Service,
    Document,
    Insured,
  },
};
</script>
<style lang="scss"></style>
