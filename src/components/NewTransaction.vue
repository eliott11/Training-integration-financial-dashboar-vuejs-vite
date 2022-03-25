<template>
  <section class="newtran">
    <div class="newtrans-section" v-for="(newTransacBlock, index) in data" :key="index"> <!--- general --->
      <div class="transcontent-left block-shadow"> <!--- content left --->
        <h4>{{newTransacBlock.h4}}</h4>
        <div class="content-top"> <!--- general img + name --->
          <!-- <div class="user-transac" v-for="(persona, index) in newTransacBlock.person" :key="index">  img + name 
            <div class="photo"><img :src="`../assets/avatar${persona.id}.png`"></div>
            <div class="textPhoto">{{persona.name}}</div>
          </div> -->
          <div class="user-transac"> <!--- img + name --->
            <div class="photo"><img src="../assets/avatar1.png"></div>
            <div class="textPhoto">{{newTransacBlock.namePerson1}}</div>
          </div>
          <div class="user-transac">
            <div class="photo"><img src="../assets/avatar2.png"></div>
            <div class="textPhoto">{{newTransacBlock.namePerson2}}</div>
          </div>
          <div class="user-transac">
            <div class="photo"><img src="../assets/avatar3.png"></div>
            <div class="textPhoto">{{newTransacBlock.namePerson3}}</div>
          </div>
          <div class="user-transac">
            <div class="photo"><img src="../assets/avatar5.png"></div>
            <div class="textPhoto">{{newTransacBlock.namePerson4}}</div>
          </div>
          <div class="user-transac">
            <div class="photo"><img src="../assets/avatar4.png"></div>
            <div class="textPhoto">{{newTransacBlock.namePerson5}}</div>
          </div>
          <div class="user-transac"> <!--- icon + description --->
            <div class="photo"><i :class="`${newTransacBlock.logoLib1} ${newTransacBlock.logoLib1}-${newTransacBlock.logo1}`"></i></div>
            <div class="textPhoto">{{newTransacBlock.addNew}}</div>
          </div>
        </div>
        <div class="btn-bottom"> <!--- button bottom --->
          <input placeholder="0                                    $">
          <button>{{newTransacBlock.textBtn}}<i class="fas fa-angle-right"></i></button>
        </div>
      </div>
      <div class="transcontent-right"> <!--- content right --->
          <div class="right-btn">
            <div><i :class="`${newTransacBlock.logoLib2} ${newTransacBlock.logo2} ${newTransacBlock.classImg1}`"></i></div>
            <div><i :class="`${newTransacBlock.logoLib2} ${newTransacBlock.logo2} ${newTransacBlock.classImg2}`"></i></div>
            <div :class="`${newTransacBlock.pClass} ${newTransacBlock.pClass}1`">{{newTransacBlock.p1}}</div>
            <div :class="`${newTransacBlock.pClass} ${newTransacBlock.pClass}2`">{{newTransacBlock.p2}}</div>
            <div :class="`${newTransacBlock.logoLib3} ${newTransacBlock.pClass2}`"></div>
          </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'NewTransaction',
  props: {
    data: {
          type: Array,
          required: true
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.newtrans-section .block-shadow {
    box-shadow: 0px 16px 24px rgba(0, 0, 0, 0.06), 0px 2px 6px rgba(0, 0, 0, 0.04), 0px 0px 1px rgba(0, 0, 0, 0.04);
    background: linear-gradient(180deg, #FFFFFF 0%, #FFFFFF 100%);
    border-radius: 28px;
    margin: 0 8px 0 5px;
    padding: 12px 15px;
}
h4 {
  margin-bottom: 4px;
}
.newtrans-section { /* content section */
  display: flex;
  color: #404040;
  justify-content: space-between;
  height: 100%;
}
.transcontent-left { /* content left */
  width: 70%;
}
.transcontent-right { /* content right */
  width: 30%;
}
.content-top { /* content top */
  display: flex;
  align-items: flex-end;
  font-size: 13.5px;
}
.photo { /* image div */
  text-align: center;
}
.photo img { /* image size */
  height: 40px;
}
.textPhoto {
  text-align: center;
}
.user-transac { /* card user margin */
  margin: 5px;
}
.bi { /* icon + */
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-content: center;
  margin: 5.2px;
  font-size: 15px;
  color: #FFC145;
}
.bi-plus-circle-fill { /* icon + */
    border-radius: 50%;
}
i.bi-plus-circle-fill::before {
    background-color: black;
    border-radius: 10px;
}
.btn-bottom { /* button bottom space between */
  display: flex;
  justify-content: space-between;
}
.btn-bottom button:hover { /* bottom menu button effect */
  background-color: white;
  color: #FFC145;
  border: 1px solid #FFC145;
  transition-duration: 0.5s;
}
input, button { /* button height */
  height: 40px;
}
input { /* input display */
  border: 1.5px solid #197BBD;
  box-sizing: border-box;
  border-radius: 8px;
  width: 60%;
}
button { /* button display */
  background: #FFC145;
  border-radius: 13.617px;
  border: none;
  font-size: 11.1442px;
  line-height: 14px;
  font-weight: normal;
  color: #404040;
  width:37%;
}
.right-btn { /* right part button */
  background: #ED654C;
  box-shadow: 0px 0px 50px rgba(0, 0, 0, 0.05);
  border-radius: 19.0044px;
  height: 100%;
  font-size: 18px;
  position: relative;
}
.text-btn-right { /* text right button */
  position: absolute;
  color: #ffffff;
  font-weight: 400;
}
.fa-chevron-right {
  position: absolute;
  color: #ffffff;
  bottom: 10px;
  margin-left: 60px;
}
.text-btn-right1 { /* text right button */
  bottom: 30px;
  margin-left: 15px;
}
.text-btn-right2 { /* text right button */
  bottom: 7px;
  margin-left: 15px;
}
.fa-bitcoin { /* icons background general*/
  font-size: 27px;
  color: #D15842;
}
.btc1 { /* icon */
  position: absolute;
  transform: rotate(-35deg);
  margin: 50px 0 0 45px;
}
.btc2 { /* icon */
  position: absolute;
  transform: rotate(20deg);
  margin: 75px 0 0 5px;
}
</style>
