<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 1</h2>
        <p>
           1. แสดงค่าจำนวนเต็มที่มากที่สุด กำหนดให้ $number = array(1,2,31,4,15,6,7,22,9,10);
        </p>
        <p>
            number = {{ number }}
        </p>
        <p>
            แสดงค่าจำนวนเต็มที่มากที่สุด = {{ maxValue }}
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            number: [1, 2, 31, 4, 15, 6, 7, 22, 9, 10],
            maxValue: 0,
        };
    },
    mounted() {
        this.maxValue=this.number[0]
        for (var i = 0; i < this.number.length; i++) {
            if (this.maxValue < this.number[i]) {
                this.maxValue = this.number[i];
            }
        }
    }
}
</script>