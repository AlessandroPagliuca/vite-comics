<template>
    <footer id="hero" class="d-flex flex-column">
        <IconsComponent />
        <div class="d-flex justify-content-between container text-white p-3">
            <div class="row">
                <!--Andremo a generare le 4 col con all'interno le ul utilizzando il v-for-->
                <div class="col-4" v-for="(linkFoot, lkT) in linksFoot" :key="lkT">
                    <h6 class="text-uppercase">{{ linkFoot.title }}</h6> 

                    <ul>
                        <!--Andremo a generare i link usando il v-for nel tag li-->
                        <li v-for="link in linkFoot.links">
                            <a class="c92Link">{{ link.footLink }}</a> 
                        </li>
                    </ul>
                </div>  
            </div>
            
            <img style="width: 16rem;" src="../assets/images/dc-logo-bg.png" alt="">
        </div>

        <div class="bg-dark">
            <div class="d-flex justify-content-between container p-3">
                <button class="btn btn-outline-primary text-white text-uppercase">sign-up now!</button>

                <div class="d-flex align-items-center">
                    <div class="text-uppercase text-primary fs-5 fw-semibold px-1">follow us</div>
                    <a class="px-1" href="#" v-for="(img, index) in linksImg" :key="index">
                        <img :src="getImageUrl(img.image)" alt="">
                    </a>
                </div>

            </div>

        </div>
    </footer>
</template>

<script>

import {images, footLinks} from '../data/data.js';
import IconsComponent from './IconsComponent.vue';

    export default {
        name: 'FooterComponent',
        components:{
            IconsComponent,
        },
        data(){
            return{
                linksImg: images,
                linksFoot: footLinks,
                count: 0,

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
        position: relative;
    };
    .c92Link{
        text-decoration: none;
        color: grey;
        cursor: pointer;

        &:hover{
            color: white;
        }
    };
   
</style>