<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 8</h2>
        <p>
            8. โปรแกรมแปลงเลขฐาน 2 เป็น เลขฐาน 10 เช่น 0111 = 7
        </p>
        <p>
            Input Root 2 = <input v-model="numberRoot2" type="String" placeholder="0" min="0" />
        </p>
        <button v-on:click="toCalculate()" class="buttonInput">Input</button>
        <p>
            Input Root 10 = {{ numberRoot10 }}
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            numberRoot2: '',
            numberRoot10: 0,
        };
    },
    methods: {
        toCalculate() {
            this.numberRoot10 = 0
            if (this.numberRoot2 > 0) {
                for (var i = this.numberRoot2.length - 1; i >= 0; i--) {
                    this.numberRoot10 += this.numberRoot2.charAt(this.numberRoot2.length - i - 1) * (2 ** i)
                }
            } else {
                console.log("กรุณาใส่ค่ามากกว่า 0")
            }
            this.numberRoot2 = ''
        }
    }
}
</script>