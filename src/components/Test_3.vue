<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 3</h2>
        <p>
            3. เรียงลำดับตัวเลขจากน้อยไปหามาก กำหนดให้ $number = array(1,2,31,4,15,6,7,22,9,10);
        </p>
        <p>
            number = [1, 2, 31, 4, 15, 6, 7, 22, 9, 10]
        </p>
        <p>
            เรียงลำดับตัวเลขจากน้อยไปหามาก = {{ numberSolt }}
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
            var minValue = this.number[0]
            for (var j = 0; j < this.number.length; j++) {
                if (minValue > this.number[j]) {
                    minValue = this.number[j]
                    numberSplice = j
                }
            }
            this.number.splice(numberSplice,1)
            return minValue
        }
    }
}
</script>