<script lang="ts">
import Bottom from './Bottom.vue';
export default{
    name: "Section",
    data() {
        
    },
    components:{
        Bottom
    }
}
</script>

<template>
   <section>
    <div class="bg"></div>
    <div class="text">
        <h1>Trucking</h1>
        <h1>Insurance</h1>
        <h1>Specialty</h1>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi cupiditate molestiae dolore dolorum quos reprehenderit voluptatum facere natus neque unde!</p>
    </div>

    <Bottom/>
   </section>
</template>

<style scoped>
    section{
        position: relative;
        width: 100vw;
    }
    .bg{
        width: 100%;
        height: 95vh;

        position: absolute;
        top: -10vw;

        background: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)), url('@/assets/img/truck_hero.jpg') no-repeat center/cover;

        z-index: -1;
    }
    .text{
        margin-top: 8vw;
        margin-left: 10vw;
    }
    .text h1{
        color: #fff;
        font-size: 5vw;
        text-transform: uppercase;
    }
    .text p {
        color: #fff;
        width: 30vw;
        margin-top: 2vw;
        font-size: 1vw;
    }
</style>