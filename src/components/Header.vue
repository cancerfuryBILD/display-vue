<template>
    <header>
        <div class="container header">
            <logo/>
            <social-links/>
            <button type="button" class="navbar-toggler collapsed" data-toggle="collapse" data-target="#navbarCollapse">
                <span class="navbar-icon"><svg height="32px" id="Layer_1" style="fill:#737373" version="1.1" viewBox="0 0 32 32" width="32px" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><path d="M4,10h24c1.104,0,2-0.896,2-2s-0.896-2-2-2H4C2.896,6,2,6.896,2,8S2.896,10,4,10z M28,14H4c-1.104,0-2,0.896-2,2  s0.896,2,2,2h24c1.104,0,2-0.896,2-2S29.104,14,28,14z M28,22H4c-1.104,0-2,0.896-2,2s0.896,2,2,2h24c1.104,0,2-0.896,2-2  S29.104,22,28,22z"/></svg></span>
            </button>
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
    padding: 30px 15px 23px 15px;

}
.header button {
        display: none;
    }
@media (max-width: 576px) {
    .container {
        overflow:hidden;
    }
    .header button {
        display: initial;
        float: right;
        margin-top: 5px;
    }
}
</style>
