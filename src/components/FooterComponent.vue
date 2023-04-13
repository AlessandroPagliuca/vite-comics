<template>
    <footer id="hero">
        <div class="d-flex justify-content-between container text-white p-3">
            <!--Andremo a generare le 4 ul utilizzando il v-for nel tag ul-->
            <ul>
                <!--Andremo a generare i link usando il v-for nel tag li-->
                <li>
                    link
                </li>
            </ul>
        </div>

        <div class="bg-dark">
            <div class="d-flex justify-content-between container p-3">
                <button class="btn btn-outline-primary text-white text-uppercase">sign up</button>

                <div class="d-flex">
                    <div class="text-uppercase text-white">follow us</div>
                    <a href="#">
                        <img src="../assets/images/footer-facebook.png" alt="">
                    </a>
                </div>

            </div>

        </div>
    </footer>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

    #hero{
        background-image: url(../assets/images/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
    }
</style>