<template>
  <p>Your Score Is: <span class='score'>{{score}}</span> ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'NinJa Fingers'
        }else if(this.score < 400){
            this.rank = 'Rapid Reflexes'
        }else{
            this.rank = 'Snail pace...'
        }
    }
}
</script>

<style>
.rank,.score{
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>