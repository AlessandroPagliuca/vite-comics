<template>
    <header>
        <div class="d-flex justify-content-between align-items-center container p-3">
            <img src="../assets/images/dc-logo.png" alt="logo-dc">

            <ul class="d-flex gap-2">
                <!-- Andremo ad inserire il => v-for=" (link, index ) in links" :key="index" <= 
                all'interno del tag li per generare la lista completa dei link  -->
                <li v-for="link in linksNav">
                    <a class="text-dark text-uppercase fw-semibold">{{ link.navLink }}</a>
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

</style>