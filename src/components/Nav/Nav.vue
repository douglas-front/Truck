<script lang="ts">
    export default{
        name: 'Nav' 
    }
</script>

<template>
   <header>
    <nav>
        <h1>Truck</h1>
        <ul>
            <li><a href="">Home</a></li>
            <li><a href="">Contact</a></li>
            <li><a href="">Trucks</a></li>
            <li><a href="">About</a></li>
            <li><a href="">References</a></li>
        </ul>
        <div class="btn_nav">
            <button>Get Products</button>
        </div>
    </nav>
   </header>
</template>

<style scoped>
    header{
        background: #fff;
        height: 9vh;
        overflow: hidden;
        position: fixed;
        width: 95vw;
        top: 2vw;
        left: 50%;
        transform: translate(-50%,-0%);

        z-index: 999;
    }
    header nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        padding-inline: 2vw;

    }
    nav ul{
        display: flex;
        gap: 3vw;
        list-style: none;
    }
    ul li a{
        position: relative;
        color: #000;
        text-decoration: none;
        font-size: 1.2vw;
    }
    ul li a::before{
        content: '';
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translate(-50%,0%);
        height: 0.15vw;
        width: 0%;
        background: #000;

        transition: all .3s;
    }
    ul li a:hover::before{
        width: 100%;
    }
    nav h1{
        font-size: 2vw;
    }
    .btn_nav{
        overflow: initial;
    }
    .btn_nav button{
        overflow: hidden;
        position: relative;
        cursor: pointer;
        padding: 0.5vw 2vw 0.5vw 2vw;

        background: transparent;
        border: 0.1vw solid #000;

        z-index: 10;
        transition: all .5s;

        font-size: 1vw;
    }
    .btn_nav button::before{
        content: '';
        width: 0%;
        height: 300%;
        position: absolute;
        left: 0;
        top: -1vw;
        background: #000;
        transform: rotate(-20deg);
        z-index: -1;

        transition: all .3s ease;
    }
    .btn_nav button::after{
        content: '';
        width: 0%;
        height: 300%;
        position: absolute;
        right: -1vw;
        top: -1vw;
        background: #000;
        transform: rotate(-20deg);
        z-index: -1;

        transition: all .3s ease;

    }
    .btn_nav button:hover::after,
    .btn_nav button:hover::before{
        width: 60%;
    }
    .btn_nav button:hover{
        color: #fff;
        transform: scale(1.1);
    }


</style>