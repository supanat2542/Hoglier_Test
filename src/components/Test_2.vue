<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 2</h2>
        <p>
            2. แสดงค่าจำนวนเต็มที่น้อยที่สุด กำหนดให้ $number = array(1,2,31,4,15,6,7,22,9,10);
        </p>
        <p>
            number = {{ number }}
        </p>
        <p>
            แสดงค่าจำนวนเต็มที่น้อยที่สุด = {{ minValue }}
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            number: [1, 2, 31, 4, 15, 6, 7, 22, 9, 10],
            minValue: 0,
        };
    },
    mounted() {
        this.minValue=this.number[0]
        for (var i = 0; i < this.number.length; i++) {
            if (this.minValue > this.number[i]) {
                this.minValue = this.number[i];
            }
        }
    }
}
</script>