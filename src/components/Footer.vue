<template>
    <section class="footer">
        <call-to-action-2 :callActionTitle="callActionTitle" />
        <footer>
            <div class="container">
                <p>COPYRIGHT 2019 DISPLAY. ALL RIGHTS RESERVED</p>
                <ul class="footer-nav">
                    <li><a href="index.html">Home </a>/</li>
                    <li><a href="about.html"> About </a>/</li>
                    <li><a href="work.html"> Work </a>/</li>
                    <li><a href="contact.html"> Contact</a></li>
                </ul>
            </div>
        </footer>
    </section>
</template>

<script>
import CallToAction2 from "@/components/CallToAction2.vue";

export default {
    name: "Footer",
    components: {
        "call-to-action-2": CallToAction2,
    },
    data() {
        return {
            callActionTitle: 'Are You Ready To Be Blown Away?'
        }
    }
}
</script>

<style>
html {
   min-height: 100%;
   position: relative;
}
.footer {
    bottom: 0;
    width: 100%;
    position: absolute;
    height: 200px;
}
footer {
    background-color: #efefef;
    padding-top: 23px;
    padding-bottom: 15px;
    font-size: 12px;
}
footer p {
    display: inline;
    font-size: 0.75rem;
}
footer p, footer a {
    color: #a5a5a5;
}
.footer-nav li {
    display: inline;
    list-style: none;
}
.footer-nav {
    float: right;
}
footer a:hover {
    text-decoration: none;
}
.footer-nav li a {
    margin: 0px 5px;
}
@media (max-width: 576px) {
    .footer-nav {
    float: none;
    padding-left: 0px;    
}
footer {
        text-align: center;
    }
}
</style>
