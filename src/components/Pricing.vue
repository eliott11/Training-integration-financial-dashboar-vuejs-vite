<template>
  <section class="pricing">
        <h4>Goals <span><i class="bi bi-plus-circle-fill"></i></span></h4>
        <div class="goals-content"> <!--- class generale --->
            <div class="pricing-block block-shadow" v-for="(pricingBlock, index) in data" :key="index"> <!--- general class card --->
                <div class="price-stats"> <!--- card content top--->
                    <span class="price-text">${{pricingBlock.price}}</span>
                    <span class="date-text">{{pricingBlock.date}}</span>
                </div>
                <div> <!--- card content bottom--->
                    <div><i :class="`${pricingBlock.logoLib} ${pricingBlock.logoLib}-${pricingBlock.logo}`"></i></div>
                    <div class="name-stats">{{pricingBlock.label}}</div>
                </div>
            </div>
            <i class="fas fa-chevron-right"></i>
        </div>
    </section>
</template>

<script>
export default {
  name: 'Pricing',
  props: {
      data: {
          type: Array,
          required: true
      }
  }
}
</script>

<style scoped>
.pricing {
    margin-left: 15px;
}
.block-shadow {
    padding: 12px 18px;
}
.bi-plus-circle-fill { /* icon + */
    font-size: 15px;
    color: #FFC145;
    border-radius: 50%;
    margin: 5px;
}
i.bi-plus-circle-fill::before {
    background-color: black;
    border-radius: 10px;
}
.goals-content { /* cards general display */
    display: flex;
    justify-content: space-between;
    height: 80%;
}
.pricing-block { /* cards display content */
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 33%;
}
.price-stats { /* price */
    color: #696969;
    display: flex;
    flex-direction: column;
}
span { /* text general */
    margin: -7px 0;
}
.price-text { /* price text */
    font-weight: 600;
    font-size: 20px;
    margin: 0;
}
.date-text { /* date text */
    color: #AEAEAE;
    font-size: 14px;
}
.fa-mountain, .fa-brush, .bi-controller { /* icons size */
    font-size: 24px;
}
.fa-mountain {          /* icons color */
    color: #6DA2E4;
}
.fa-brush {
    color: #F17F29;
}
.bi-controller {
    color: #1E9540;
}
.name-stats {
    color: #404040;
}
.fas {
    display: flex;
    align-items: center;
    padding: 5px;
    color: #197BBD;
}
i.fas {
  font-size: 20px;
}
</style>
