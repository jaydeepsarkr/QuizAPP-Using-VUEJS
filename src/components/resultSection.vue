<template>
  <div class="result">
        <div class="title">{{ results[resultINDEX].title }}</div>
        <div class="desc">
           {{ results[resultINDEX].desc }}
        </div>
    </div>
</template>

<script>
export default {

    props:["totalCorrect","results"],
    computed: {
        resultINDEX(){
             let index = 0;

             this.results.forEach((e,i)=>{
                if(e.min<=this.totalCorrect&&e.max>=this.totalCorrect){
                    index = i;

                }
             })
             return index;
        }


    }


}
</script>
