<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 9</h2>
        <p>
            9. โปรแกรมแปลงเลขฐาน 10 เป็น เลขฐาน 2 เช่น 30 = 11110
        </p>
        <p>
            Input Root 10 = <input v-model="numberRoot10" type="String" placeholder="0" />
        </p>
        <button v-on:click="toCalculate()" class="buttonInput">Input</button>
        <p>
            Input Root 2 = {{ numberRoot2 }}
        </p>

    </div>
</template>

<script>
export default {
    data() {
        return {
            numberRoot10: '',
            numberRoot2: '0',
        };
    },
    methods: {
        toCalculate() {
            this.numberRoot2 = '0'
            if (this.numberRoot10 > 0) {
                do {
                    var result = this.numberRoot10 % 2
                    this.numberRoot2 = result + this.numberRoot2
                    if (result == 0) {
                        this.numberRoot10 = this.numberRoot10 / 2
                    } else {
                        this.numberRoot10 = (this.numberRoot10 - 1) / 2
                    }
                } while (this.numberRoot10 > 0)
            } else {
                this.numberRoot10 = 0
                console.log("กรุณาใส่ค่ามากกว่า 0")
            }
        }
    }
}
</script>