<script lang="ts">
import { defineComponent } from 'vue'
import Button from '../Button/Button.vue'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

// Registrando o plugin ScrollTrigger
gsap.registerPlugin(ScrollTrigger)

export default defineComponent({
  components: {
    Button
  },
  mounted() {
    const animation = () => {
      gsap.to('.truck_img', {
        y: '-10%',
        delay: 0.2,
        opacity: 1,
        borderRadius: "0%"
      })

      gsap.to('.animation_p_up', {
        y: '-40%',
        delay: 0.5,
        opacity: 1
      })
      gsap.to('.animation_h1_up', {
        y: '-5%',
        delay: 0.8,
        opacity: 1
      })
      gsap.to('.animation_p_up_second', {
        y: '-30%',
        delay: 0.9,
        opacity: 1
      })
      gsap.to('.animation_button_up', {
        y: '-30%',
        delay: 1,
        opacity: 1
      })
    }


    // Aguarde o próximo frame para garantir que os elementos estejam disponíveis
    this.$nextTick(() => {
      ScrollTrigger.create({
        trigger: '.s',
        markers: true,
        onEnter: () => animation(),
        start: '-320vw'
      })
    })
  }
})
</script>

<template>
  <section class="s">
    <div class="container">
      <div class="text">
        <p class="animation_p_up">Lorem, ipsum dolor.</p>
        <h1 class="animation_h1_up">We make insurance companies complete for you business</h1>
        <p class="animation_p_up_second">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Inventore animi ullam beatae
          assumenda amet sed dolor nobis commodi quia vitae blanditiis officia, recusandae tempore
          nam accusamus corrupti molestias fugit natus at, dolorem repellat odio quae. Veritatis
          omnis explicabo id magnam.
        </p>
        <div class="animation_button_up">
          <Button :BgColor="'gray'" :Color="'#fff'" :Text="'LETS TALK'" />
        </div>
      </div>

      <div class="img truck_img">
        <img src="../../assets/img/truckSecondSection.webp" alt="truck" />
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  margin-top: 7vw;
  height: 100vh;
}
.container {
  display: flex;
  justify-content: space-between;
  padding-inline: 8vw;
}
.text {
  width: 35vw;
  display: flex;
  flex-direction: column;
}
.text h1 {
  font-size: 3vw;
  opacity: 0;

}
.text p,
.text div {
  margin-top: 2vw;
  font-size: 1vw;
  opacity: 0;

}
.img img {
  width: 40vw;
  height: 70vh;
  object-fit: cover;
}
.img{
  overflow: hidden;
  opacity: 0;
  border-radius: 50%;
}
</style>
