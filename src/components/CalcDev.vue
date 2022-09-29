<template>
    <div class="calculator">
        <div class="display">{{current || '0'}}</div>
        <div @click="clear" class="btn">C</div>
        <div @click="sign" class="btn">+/-</div>
        <div class="btn">%</div>
        <div class="btn operator">/</div>
        <div class="btn">7</div>
        <div class="btn">8</div>
        <div class="btn">9</div>
        <div class="btn operator">*</div>
        <div class="btn">4</div>
        <div class="btn">5</div>
        <div class="btn">6</div>
        <div class="btn operator">-</div>
        <div class="btn">1</div>
        <div class="btn">2</div>
        <div class="btn">3</div>
        <div class="btn operator">+</div>
        <div class="btn zero">0</div>
        <div class="btn">.</div>
        <div class="btn operator">=</div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            current: '1234',
        }
        
    },
    /*******To define function you add a method */

    methods: {
        clear() {
            this.current = '';
        },
        sign() {
            this.current = this.current.charAt(0) === '-'?
              this.current.slice(1) : '-';
        }
    }
}
</script>

<style scoped>
    .calculator{
        width: 400px;
        margin: 0 auto;
        font-size: 40px;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: minmax(50px, auto);
    }

    .display{
        grid-column: 1 / 5;
        background-color: #333;
        color: #ffff;
    }

    .zero{
        grid-column: 1 / 3;
    }

    .btn{
        background-color: #F2F2F2;
        border: 1px solid #3333;
    }

    .operator{
        background-color: orange;
        color: white;
    }

</style>