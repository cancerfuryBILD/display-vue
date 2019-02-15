<template>
    <div class="action-call-2">
        <div class="container">
            <h4>{{callActionTitle}}</h4>
            <action-button :buttonTitle="buttonTitle" :buttonType="buttonType" :buttonLink="buttonLink"/>
        </div>
    </div>
</template>

<script>
import ActionButton from "@/components/ActionButton.vue";

export default {
    name: "CallToAction2",
    components: {
        'action-button': ActionButton
    },
    props: ['callActionTitle'],
    data() {
        return {
            buttonTitle: 'Click here to find out',
            buttonType: 'button',
            buttonLink: '/work'
        }
    }
}
</script>

<style>
.action-call-2 {
    background-color: #322f2f;
    padding: 54px 0px 56px 0px;
}
.action-call-2 .action-btn {
    float: right;
}
h4 {
    display: inline;
    color: #fff;
}
</style>
