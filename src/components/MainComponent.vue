<template>
    <main>
        <div class="bg-dark">
            <div class="container text-white p-3">
                -- Content goes here -- 
            </div>
        </div>
        <!--In questo punto verrà aggiunto il componente delle icone-->
        <IconsComponent />
    </main>
</template>

<script>
import IconsComponent from './IconsComponent.vue';
    export default {
        name: 'MainComponent',
        components:{
            IconsComponent,
        }

        
    }
</script>

<style lang="scss" scoped>

</style>