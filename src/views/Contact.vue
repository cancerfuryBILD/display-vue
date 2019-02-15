<template>
  <div>
    <page-title :headline="headline"/>
    <geo-map/>
    <div class="container contact-form">
      <contact-form/>
      <contact-info/>
    </div>
  </div>
</template>

<script>
import GeoMap from '@/components/GeoMap.vue';
import PageTitle from '@/components/PageTitle.vue';
import ContactForm from '@/components/ContactForm.vue';
import ContactInfo from '@/components/ContactInfo.vue';
export default {
  name: "contact",
  components: {
    'geo-map': GeoMap,
    'page-title': PageTitle,
    'contact-form': ContactForm,
    'contact-info': ContactInfo
  },
  data() {
    return {
      headline: 'Got a question or inquery?'
    }
  }
};
</script>

<style>

</style>
