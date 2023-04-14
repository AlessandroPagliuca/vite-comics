<template>
    <main>
        <div class="bg-dark">
            <div class="container text-white p-3">
                <div class="row">
                    <div class="col-12 col-sm-6 col-md-4 col-lg-3 gap-2 d-flex justify-content-center align-items-center" v-for="(card, c) in cardComics" :key="c">
                        <div style="width: 10rem;">
                            <img class="card-img-top" :src="card.thumb" alt="">
                            <div class="card-body">
                                <p class="card-text ">{{ card.series }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import {comics} from '../data/data.js'
    export default {
        name: 'MainComponent',
        components:{
        },
        data(){
            return{
                cardComics: comics,
            }
        }

        
    }
</script>

<style lang="scss" scoped>

</style>