<template>
    <div class="result">Reaction Time: {{ score }} ms</div>
    <p class="rank">{{ rank }}</p>
</template>
<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null,
        };
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Ninja Fingers';
        } else if (this.score < 400) {
            this.rank = 'Rapid Reflexes';
        } else {
            this.rank = 'Snail Pace...';
        }
    },
};
</script>
<style>
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
.result {
    width: 200px;
    border-radius: 20px;
    background: #dfe0e0;
    box-shadow: 5px 5px 5px grey;
    color: black;
    text-align: center;
    padding: 20px 0;
    margin: 40px auto;
}
</style>
