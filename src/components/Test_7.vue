<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 7</h2>
        <p>
            7. จากสูตร a^2 + b^2 = c^2 ให้หาค่าด้านตรงข้ามมุมฉากของ สามเหลี่ยม โดยให้ input เป็นค่า a และ b และผลลัพธ์เป็นค่า c
        </p>
        <p>
            Input A = <input v-model="numberA" type="number" placeholder="0" min="1"/>
        </p>
        <p>
            Input B = <input v-model="numberB" type="number" placeholder="0" min="1"/>
        </p>
        <button class="buttonInput" v-on:click="toCalculate()">Calculate</button>
        <p>
            Result C = {{ numberC }}
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            numberA: '',
            numberB: '',
            numberC: 0,
        };
    },
    methods:{
        toCalculate(){
            if(this.numberA>0&&this.numberB>0){
                var num = (this.numberA**2)+(this.numberB**2)
               this.numberC =  Math.sqrt(num)
            }else{
                this.numberA=''
                this.numberB=''
                console.log("กรุณาใส่ค่า A & B มากกว่า 0")
            } 
        }
    }
}
</script>