<template>
    <div class="block" v-if="showBlock">
        Click me
    </div>
</template>

<script>
export default {
    props: ['delay'],
    data() {
        return {
            showBlock: false
        }
    },
    mounted() {
        console.log('component mounted')
        setTimeout(() => {
            this.showBlock = true
            console.log(this.delay)
        }, this.delay)
    },
    updated() {
    }
}
</script>

<style>
.block {
    background: #0faf87;
    border-radius: 20px;
    color: white;
    margin: 40px auto;
    padding: 100px 0;
    text-align: center;
    width: 400px;
}
</style>