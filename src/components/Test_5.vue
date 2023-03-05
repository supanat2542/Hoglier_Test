<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 5</h2>
        <p>
            5. หาจำนวนเฉพาะที่อยู่ระหว่าง 0 ถึง 500
        </p>
        <p>
            จำนวนเฉพาะที่อยู่ระหว่าง 0 ถึง 500 = {{ onlyNUmber }}
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            number: 500,
            onlyNUmber:[]
        };
    },
    mounted() {
        this.maxValue = this.number[0]
        for (var i = 2; i <= this.number; i++) {
            for (var j = 2; j <= i; j++) {
                if(i%j==0){
                    break
                }else if(j==i-1){
                    this.onlyNUmber.push(i)
                    break
                }
            }
        }
    }
}
</script>