<template>
    <header>
        <div class="d-flex justify-content-between container">
            <div class="c92HeaderImg align-self-center">
                <img src="../assets/images/dc-logo.png" alt="logo-dc">
            </div>

            <ul class="d-flex">
                <!-- Andremo ad inserire il => v-for=" (link, index ) in links" :key="index" <= 
                all'interno del tag li per generare la lista completa dei link  -->
                <li v-for="link in linksNav">
                    <div class="c92LinkBox p-2 d-flex align-items-center">
                        <a class="text-dark text-uppercase fw-semibold ">{{ link.navLink }}</a>
                    </div>
                </li>
            </ul>
        </div> 
    </header>
</template>

<script>

    import {navLinks} from '../data/data.js';
    export default {
        name: 'HeaderComponent',
        data(){
            return{
                linksNav: navLinks,
            }
        }
        
    }
</script>

<style lang="scss" scoped>
    header{
        width: 100%;
        height: 100px;
        background-color: white;
        position: fixed;
        display: flex;
        z-index: 1000;

        .c92HeaderImg{
            width: 80px;
            height: 80px;

            img{
                width: 100%;
                height: 100%;
            }
        };
        .c92LinkBox{
            height: 100px;
            cursor: pointer;

            a{
                text-decoration: none;
            };

            &:hover{
                border-bottom: 5px solid #0d6efd;

            }
        }

    }

</style>