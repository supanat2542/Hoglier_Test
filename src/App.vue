<script setup>
 import Test1 from './components/Test_1.vue'
 import Test2 from './components/Test_2.vue'
 import Test3 from './components/Test_3.vue'
 import Test4 from './components/Test_4.vue'
 import Test5 from './components/Test_5.vue'
 import Test6 from './components/Test_6.vue'
 import Test7 from './components/Test_7.vue'
 import Test8 from './components/Test_8.vue'
 import Test9 from './components/Test_9.vue'
 import Test10 from './components/Test_10.vue'
 import Testbonus from './components/Test_bonus.vue'
</script>

<template>

  <header class="logo">
    <h1 >Hoglier Test</h1>
  </header>
  <section>
    <button v-on:click=" toSelect(1)">Test 1</button>
    <button v-on:click=" toSelect(2)">Test 2</button>
    <button v-on:click=" toSelect(3)">Test 3</button>
    <button v-on:click=" toSelect(4)">Test 4</button>
    <button v-on:click=" toSelect(5)">Test 5</button>
    <button v-on:click=" toSelect(6)">Test 6</button>
    <button v-on:click=" toSelect(7)">Test 7</button>
    <button v-on:click=" toSelect(8)">Test 8</button>
    <button v-on:click=" toSelect(9)">Test 9</button>
    <button v-on:click=" toSelect(10)">Test 10</button>
    <button v-on:click=" toSelect(11)">Test Bonus</button>
  </section>
  <aside>
    <div >
      <Test1 v-if="showTest==1" />
      <Test2 v-if="showTest==2" />
      <Test3 v-if="showTest==3" />
      <Test4 v-if="showTest==4" />
      <Test5 v-if="showTest==5" />
      <Test6 v-if="showTest==6" />
      <Test7 v-if="showTest==7" />
      <Test8 v-if="showTest==8" />
      <Test9 v-if="showTest==9" />
      <Test10 v-if="showTest==10" />
      <Testbonus v-if="showTest==11" />
    </div>
  </aside>

</template>

<script>
  export default {
    data() {
        return {
            showTest: 0,
        };
    },
    methods:{
        toSelect(selecter){
          this.showTest=selecter
        }
    }
}
</script>

