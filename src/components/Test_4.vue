<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 4</h2>
        <p>
            4. เรียงลำดับตัวเลขจากมากไปหาน้อย กำหนดให้ $number = array(1,2,31,4,15,6,7,22,9,10);
        </p>
        <p>
            number = [1, 2, 31, 4, 15, 6, 7, 22, 9, 10]
        </p>
        <p>
            เรียงลำดับตัวเลขจากมากไปหาน้อย = {{ numberSolt }}
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            number: [1, 2, 31, 4, 15, 6, 7, 22, 9, 10],
            numberSolt: [],
        };
    },
    mounted() {
        var countLoop = this.number.length
        for (var i = 0; i < countLoop; i++) {
            this.numberSolt.push(this.compare())
        }
    },
    methods: {
        compare() {
            var numberSplice 
            var maxValue = this.number[0]
            for (var j = 0; j < this.number.length; j++) {
                if (maxValue < this.number[j]) {
                    maxValue = this.number[j]
                    numberSplice = j
                }
            }
            this.number.splice(numberSplice,1)
            return maxValue
        }
    }
}
</script>