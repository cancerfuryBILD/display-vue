<template>
  <div class="about">
    <page-title :headline="headline"/>
    <about-main/>
    <div>
        <about-article :articleTexts="articleTexts" />
    </div>
    <about-services></about-services>
  </div>
</template>

<script>
import PageTitle from "@/components/PageTitle.vue";
import AboutMain from "@/components/AboutMain.vue";
import AboutArticle from "@/components/AboutArticle.vue";
import Services from "@/components/Services.vue";
export default {
  name: 'about',
  components: {
    'page-title': PageTitle,
    'about-main': AboutMain,
    'about-article': AboutArticle,
    'about-services': Services
  },
  data() {
    return {
      headline: 'About my business', // Headline for PageTitle component
      articleTexts: [`<h2>Mission Statement</h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque eu 
                erat lacus, vel congue mauris. Fusce velit justo, faucibus eu sagittis ac, 
                gravida quis tortor. Suspendisse non urna mi, quis tincidunt eros. Nullam 
                tellus turpis, fringilla sit amet congue ut, luctus a nulla. Donec sit amet 
                sapien neque, id ullamcorper diam. Nulla facilisi. Pellentesque pellentesque 
                arcu a elit congue lacinia.</p>`,
                `<h2>Fun Facts</h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque eu erat 
                lacus, vel congue mauris. Fusce velit justo, faucibus eu sagittis ac, gravida 
                quis tortor. Suspendisse non urna mi, quis tincidunt eros. Nullam tellus turpis, 
                fringilla sit amet congue ut, luctus a nulla. Donec sit amet sapien neque, id 
                ullamcorper diam. Nulla facilisi. Pellentesque pellentesque arcu a elit congue lacinia.</p>`
      ]
    }
  }
}
</script>

<style>
.about {
  clear: right;
  margin-bottom: 44px;
}
</style>