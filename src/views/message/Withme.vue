<template>
 <div id="withme">
  <div id='messageTitle'>
   <span style="margin-left: .1rem" @click="back" ><-</span>
   <h5>@{{pagemessage.withme}}</h5>
  </div>
  <div class="titlehead">
   < img class="messagehead" src="../../assets/img/messagesHead.png" alt="">
   <ul>
    <li>
     {{pagemessage.withmepersonA}}
    </li>
    <li>
     5-22 16:40
    </li>
   </ul>
  </div>
  <p>//@{{pagemessage.withmepersonA}} ：{{pagemessage.withmetransfert}}</p >
  <div class="messagecontain">
   < img class="messageconent" src="../../assets/img/messageConent.png" alt="">
   <div class="containtext">
    <span>@{{pagemessage.withmepersonB}}</span>
    <div class="containtext">{{pagemessage.withmecorn}}
    </div>
   </div>
  </div>
  <div class="titlehead">
   < img class="messagehead" src="../../assets/img/messagesHead.png" alt="">
   <ul>
    <li>
     {{pagemessage.withmepersonA}}
    </li>
    <li>
     5-22 16:40
    </li>
   </ul>
  </div>
  <p>{{pagemessage.withmecomment}}@{{pagemessage.withmepersonA}}</p >
  <div class="messagecontain">
   < img class="messageconent" src="../../assets/img/messageConent.png" alt="">
   <div class="containtext">
    <span>@{{pagemessage.withmepersonC}}</span>
    <div class="containtext">
     {{pagemessage.withmerice}}
    </div>
   </div>
  </div>
 </div>
</template>
<script>
    export default {
        data(){
            return{
                pagemessage:{
                    withmepersonA:this.$t("message.withmepersonA"),
                    withmepersonB:this.$t("message.withmepersonB"),
                    withmepersonC:this.$t("message.withmepersonC"),
                    withmecorn:this.$t("message.withmecorn"),
                    withmerice:this.$t("message.withmerice"),
                    withmecomment:this.$t("message.withmecomment"),
                    withme:this.$t("message.withme"),
                    withmetransfert:this.$t("message.withmetransfert")
                },

            }
        },
        methods:{
            back(){
                this.$router.push('/message');
                this.$emit('returnM')
            }
        }

    }

</script>

<style scoped>
 h5{
  float: right;
  margin-right: 3.1rem;
 margin-top: 0.01rem;
 }
.messagehead{
 width:.7rem!important;
 height: .7rem!important;
}
 .messageconent{
  width: 1.2rem;
  height: 1.2rem;
 }
 h6{
  display: inline;
  margin: 0 10rem;
 }
 ul{
  float: right;

 }
 .titlehead{
  display: flex;
  flex-direction: row;
 }
 .messagecontain{
  display: flex;
  flex-direction: row;
  background-color: #f2f2f5;
  padding-bottom: .3rem;
  border-bottom: .01rem solid #ccc;
  margin-bottom: .5rem;
  padding-top: .2rem;

 }
 .containtext{
  display: flex;
  flex-direction: column;
  margin-left: .2rem;
  margin-right: .1rem;
  height: 1.3rem;
  text-overflow: ellipsis;
  overflow: hidden;
 }
 #withme{
  margin:0 .1rem;
 }
 #messageTitle{
  width: 100%;
  background-color: #0086b3;
  margin-bottom: .2rem;
 }
</style>