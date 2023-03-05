<template>
    <div class="bodyQuest">
        <h2 class="mainQuest">Test 10</h2>
        <p>
            10. กำหนดให้ $matrixA และ  $matrixB จงหาค่า $matrixA + $matrixB
        </p>
        <p> matrixA  = {{ matrixA }}<br/> <br/> matrixB  = {{ matrixB }}<br/> <br/>matrixC  = {{ matrixC }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            matrixA:[
                [1,2,3],
                [4,5,6],
                [7,8,9]
            ],
            matrixB:[
                [1,1,1],
                [1,1,1],
                [1,1,1]
            ],
            matrixC:[]
        };
    },
    mounted() {
        for(var i = 0; i < this.matrixA.length; i++){
            this.matrixC.push([])
            for(var j = 0; j < this.matrixA[i].length; j++){
                this.matrixC[i][j]= this.matrixA[i][j]+this.matrixB[i][j]
            }
        }
    }
}
</script>