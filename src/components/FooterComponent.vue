<template>
    <footer id="hero">
        <IconsComponent />
        <div class="d-flex justify-content-between container text-white p-3">
            <!--Andremo a generare le 4 ul utilizzando il v-for nel tag ul-->
            <ul>
                <!--Andremo a generare i link usando il v-for nel tag li-->
                <li>
                    link
                </li>
            </ul>
            <img src="../assets/images/dc-logo-bg.png" alt="">
        </div>

        <div class="bg-dark">
            <div class="d-flex justify-content-between container p-3">
                <button class="btn btn-outline-primary text-white text-uppercase">sign-up now!</button>

                <div class="d-flex align-items-center">
                    <div class="text-uppercase text-primary fs-5 fw-semibold px-1">follow us</div>
                    <a class="px-1" href="#" v-for="(img, index) in linkImg" :key="index">
                        <img :src="getImageUrl(img.image)" alt="">
                    </a>
                </div>

            </div>

        </div>
    </footer>
</template>

<script>

import {images} from '../data/data.js';
import IconsComponent from './IconsComponent.vue';

    export default {
        name: 'FooterComponent',
        components:{
            IconsComponent,
        },
        data(){
            return{
                linkImg: images,

            }
        },
        methods:{
            getImageUrl(img) {
                return new URL(`../assets/images/${img}`, import.meta.url).href;
            }

        }
    }
</script>

<style lang="scss" scoped>

    #hero{
        background-image: url(../assets/images/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
    }
</style>