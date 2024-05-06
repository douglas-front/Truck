<script lang="ts">
import Button from '../../..//components/Button/Button.vue'
export default {
  name: 'Bottom',
  data() {
    return{
      imgs: [
      {
        n: '01',
        img: '/src/assets/img/truck_hover1.jpg',
        text: "Truck Hability Insurance"
      },
      {
        n: '02',
        img: '/src/assets/img/truck_hover2.jpg',
        text: "Truck Hability Insurance"
      },
      {
        n: '03',
        img: '/src/assets/img/truck_hover3.jpg',
        text: "Truck Hability Insurance"
      }
    ]
    }
  },
  components: {
    Button
  }
}
</script>

<template>
  <div class="bottom">
    <div class="btns">
      <Button :BgColor="'#000'" :Color="'#fff'" :Text="'get a truck'" />
      <Button :BgColor="'gray'" :Color="'#fff'" :Text="'get a truck'" />
    </div>
    <div class="card">
      <div class="text">
        <h1>Insurance we offer</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe laboriosam at ipsam quam
          corporis quas provident eum perferendis non voluptatibus?
        </p>
      </div>

      <div class="conatiner_img" >
        <div class="img" v-for="item in imgs" :key="item.n">
          <h1>{{ item.n }}</h1>
          <img :src="item.img" alt="truck">
          <h2>{{ item.text }}</h2>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bottom {
  margin-top: 5vw;
  overflow: initial;
  position: relative;
  width: 100%;
  height: 40vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-inline: 1vw;
}
.card {
  box-shadow: 0px 10px 10px rgb(0 0 0 / 0.2);

  width: 100vw;
  height: 100%;
  background: #fff;
 
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.card .text {
  width: 40vw;
}
.text p {
  margin-top: 1vw;
  font-size: 1vw;
}
.text h1 {
  font-size: 2vw;
}
.btns {
  position: absolute;
  left: 9vw;
  top: -2.1vw;
  display: flex;
  gap: 2vw;
}

.conatiner_img{
  display: flex;
  gap: 0.3vw;
}
.img{
  position: relative;
  overflow: hidden;
  width: 5vw;
  height: 35vh;

  transition: all .3s;
}
.img h1{
  color: #fff;
  position: absolute;
  left: 0.4vw;
  font-size: 1.5vw;
}
.img h2{
  position: absolute;
  left: 0.4vw;
  bottom: 0.4vw;
  font-size: 1.8vw;
  color: #fff;
  opacity: 0;
  transition: all .5s;
}
.img img{
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.img:hover{
  width: 20vw;
}
.img:hover h2{
  opacity: 1;
}

</style>
