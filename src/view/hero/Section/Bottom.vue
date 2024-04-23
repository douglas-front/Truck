<script lang="ts">
import Button from '../../../components/Button/Button.vue'

export default {
  name: 'Bottom',

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
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe laboriosam at ipsam quam corporis quas provident eum perferendis non voluptatibus?
        </p>
      </div>
      <div class="img">
        <img src="" alt="">
      </div>
    </div>
  </div>
</template>

<style scoped>
.bottom {
  overflow: initial;
  position: relative;
  width: 100%;
  display: grid;
  justify-content: space-around;
  place-items: center;
}
.card {
  margin-top: 3vw;
  width: 95vw;
  height: 30vh;
  background: #fff;

  display: flex;
  align-items: center;
}
.card .text{
    width: 40vw;
    padding-left: 7vw;
}
.text p{
    margin-top: 1vw;
    font-size: 1vw;
}
.text h1{
    font-size: 2vw;
}
.btns {
  position: absolute;
  left: 9vw;
  top: 1.3vw;
  display: flex;
  gap: 2vw;
}
</style>
