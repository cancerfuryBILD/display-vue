<template>
<div class="services-section">
    <div class="container">
        <b-tabs>
            <b-tab title="first" active>
                <br>I'm the first fading tab
            </b-tab>
            <b-tab title="second" >
                <br>I'm the second tab content
            </b-tab>
            <b-tab title="disabled" disabled>
                <br>Disabled tab!
            </b-tab>
        </b-tabs>
    </div>
</div>
</template>

<script>
export default {
    name: 'Services'
}
</script>

<style>
.services-section {
    margin-top: 22px;
}
.services {
    background-color: #efefef;
    margin-bottom: 23px;
    margin-top: 26px;
}
.nav-pills {
    width: 100%;
}
.nav-pills li {
    padding: 0px;
}
.nav-pills a {
    padding: 34px 0px;
}
.nav-pills .nav-link {
    border-radius: 0px;
}
.nav-pills .nav-link.active{
    background-color: #dadada;
}
.websites, 
.photography, 
.seo, 
.applications {
    height: 90px;
    background-repeat: no-repeat;
    background-position: center;
    margin: 0px auto 5px;
    padding: 0px;
}
.websites {
    background-image: url(../assets/websites.svg);
}
.photography {
    background-image: url(../assets/photography.svg);
}
.seo {
    background-image: url(../assets/seo.svg);
}
.applications {
    background-image: url(../assets/applications.svg);
}
.h3-push {
    margin-bottom: 16px;
}
.services-list{
    margin: 16px 18px 0px;
    line-height: 25px;
}
.services-list img {
    margin-right: 12px;
}
.services-info {
    margin-bottom:  42px;
    min-height: 158px;
}
</style>
