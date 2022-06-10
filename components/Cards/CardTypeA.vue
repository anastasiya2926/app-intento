<template>
    <div class="card card_a">
        <div class="picture">
            <img :src="picture" :alt="title">
        </div>
        <div class="content">
            <h3 class="title">{{title}}</h3>
            <div class="text">{{text}}</div>
            <div class="ctas">
                <ButtonBase>{{buttonContent}}</ButtonBase>
            </div>
        </div>
    </div>
</template>

<script>
import ButtonBase from "../Dsys/ButtonBase.vue";

export default {
    components: { ButtonBase }, 
    props: {
        picture: {type: String, default: ""}, 
        title: {type: String, required: true}, 
        text: {type: String, required: true}, 
        buttonContent: {type: String, required: true}
    }
}
</script>

<style>

</style>