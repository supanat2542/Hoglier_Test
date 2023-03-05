<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test Bonus</h2>
        <p>
            แสดงผลดาว (*) ให้เป็นรูปกากบาท โดยมี input เป็นจำนวนแถวของดาว
        </p>
        <h3 v-for="number in matrix" :key = "number">
            {{ number }}
        </h3>
        <p>
            เพื่อตรวจคำตอบใน Conole  == >
        </p>

    </div>
</template>

<script>
export default {
    data() {
        return {
            numbers: 5,
            matrix: []
        };
    },
    mounted() {
        for (var i = 0; i < this.numbers; i++) {
            var result = ''
            for (var j = 0; j < this.numbers; j++) {
                var spot = i+j
                if(spot==this.numbers-1){
                    result = result + " * "
                }else if(i==j){
                    result = result + " * " 
                }else{
                    // result = result + "   " 
                    result = result + " . "
                }
            }
            this.matrix.push(result)
            console.log(result)
        }
    }
}
</script>