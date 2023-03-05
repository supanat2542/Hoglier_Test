<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 6</h2>
        <p>
            6. แสดงค่า factorial ใส่จำนวนเต็ม 5 ให้แสดงค่าของ 5! ว่ามีค่าเท่าไหร่
        </p>
        <p>
            แสดงค่า 5! = {{ result }}
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            number: 5,
            result: 1,
        };
    },
    mounted() {
        for (var i = 0; i < this.number; i++) {
            this.result = this.result*(this.number-i)
        }
    }
}
</script>