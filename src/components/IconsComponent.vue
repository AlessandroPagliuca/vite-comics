<template>
    <div class="bg-primary">
        <div class="container p-3">
            <div class="row justify-content-center">
                <div class="col-12 col-md-6 col-lg-auto d-flex align-items-center justify-content-center gap-3 c92Cursor" v-for="(icon, i) in linkIcon" :key="i">
                        <div class="c92Card">
                            <img :src="getImageUrl(icon.image)" alt="">
                        </div>

                        <span class="text-white text-uppercase"> {{ icon.title }} </span>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import {icons} from '../data/data.js';

    export default {
        name: 'IconsComponent',
        data(){
            return{
                linkIcon: icons,

            }
        },
        methods:{
            getImageUrl(icon) {
                return new URL(`../assets/images/${icon}`, import.meta.url).href;
            }

        }
    }
</script>

<style lang="scss" scoped>

    .c92Card{
        img{
            width:50px;
        }
    }

    .c92Cursor{
        cursor: pointer;
    }

</style>