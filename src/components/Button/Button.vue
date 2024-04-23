<script lang="ts">
export default {
    name: "Button",
    props:{
        BgColor: String,
        Color: String,
        Text: String
    }
}
</script>
<template>
    <button :style="{ background: BgColor, color: Color }">{{ Text }}</button>
</template>

<style scoped>
    button{
        cursor: pointer;
        padding: 1.2vw 4vw;
        border: none;
        font-size: 1vw;

        
    }
</style>