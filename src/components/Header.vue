<template>
    <header>
        <div class="container header">
                <logo/>
                <social-links/>
               
            <main-navigation/>
        </div>
    </header>
</template>

<script>
import MainNavigation from "@/components/MainNavigation.vue";
import Logo from "@/components/Logo.vue";
import SocialLinks from "@/components/SocialLinks.vue";

export default {
    name: 'Header',
    components: {
        "main-navigation": MainNavigation,
        "logo": Logo,
        'social-links': SocialLinks
    }
}
</script>

<style>

.header {
    padding: 30px 15px 15px 15px;

}
@media (max-width: 576px) {
    .container {
        overflow:hidden;
    }
}
</style>
