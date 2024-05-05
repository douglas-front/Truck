<script lang="ts">
import { defineComponent } from 'vue'
import Button from '../Button/Button.vue';
export default defineComponent({
  components:{
    Button
  }
})
</script>

<template>
  <section data-scroll-section>
    <div class="container">
      <div class="text">
        <p>Lorem, ipsum dolor.</p>
        <h1>We make insurance companies complete for you business</h1>
        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Inventore animi ullam beatae
          assumenda amet sed dolor nobis commodi quia vitae blanditiis officia, recusandae tempore
          nam accusamus corrupti molestias fugit natus at, dolorem repellat odio quae. Veritatis
          omnis explicabo id magnam.
        </p>
        <div>
            <Button :BgColor="'gray'" :Color="'#fff'" :Text="'LETS TALK'"/>
        </div>
      </div>

      <div class="img">
        <img src="../../assets/img/truckSecondSection.webp" alt="truck">
      </div>
    </div>
  </section>
</template>

<style scoped>
 section{
    margin-top: 7vw;
    height: 100vh;
 }
 .container{
    display: flex;
    justify-content: space-between;
    padding-inline: 8vw;
 }
 .text{
    width: 35vw;
    display: flex;
    flex-direction: column;
 }
 .text h1{
    font-size: 3vw;
}
.text p,
.text div{
    margin-top: 2vw;
    font-size: 1vw;
}
 .img img{
    width: 40vw;
    height: 70vh;
    object-fit: cover;
 }
</style>