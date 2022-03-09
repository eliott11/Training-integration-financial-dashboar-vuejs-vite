<template>
  <section class="cards block-shadow">
    <h4>Cards</h4>
    <div class="content-card" v-for="(cardsBlock, index) in data" :key="index">
      <div class="content-usercard">
        <div class="arrow">
          <i :class="`${cardsBlock.logoLib} ${cardsBlock.logo}-${cardsBlock.logoLeft}`"></i>
        </div>
        <div class="top-info"> <!--- Infos top --->
          <div class="card-user"> <!--- Infos card left --->
            <div class="card-account">
              <div>{{cardsBlock.namecard}}</div>
              <div class="premium">{{cardsBlock.statusAccount}}</div>
            </div>
            <div class="card-number">
              <span>{{cardsBlock.numbercards1}}</span>
              <span>{{cardsBlock.numbercards2}}</span>
              <span>{{cardsBlock.numbercards2}}</span>
              <span>{{cardsBlock.numbercards3}}</span>
            </div>
            <div class="bot-card">
              <div class="holder">
                <div class="stats-bot-card">{{cardsBlock.cardHolder}}</div>
                <div class="name-bot-card">{{cardsBlock.nameHolder}}</div>
              </div>
              <div class="expire">
                <div class="stats-bot-card">{{cardsBlock.expireDate}}</div>
                <div class="name-bot-card">{{cardsBlock.date}}</div>
              </div>
            </div>
          </div>
          <div class="bot-info"> <!--- Infos bottom --->
            <div>
              <div class="bar-progress">
                <div class="progress  mb-1"> <!--- progress bar --->
                  <div class="progress-bar-card" role="progressbar" aria-valuenow="74" aria-valuemin="0" aria-valuemax="100"></div>
                </div>
              </div>
              <div class="stats-bar">
                <span class="limit-text">{{cardsBlock.weeklySpendTitle}}</span>
                <span class="weekly-numbers">{{cardsBlock.weeklySpendAmount}}</span>
              </div>
            </div>
          </div>
        </div>
        <div class="arrow">
          <i :class="`${cardsBlock.logoLib} ${cardsBlock.logo}-${cardsBlock.logoRight}`"></i>
        </div>
        <div class="bar-card-right"></div>
      </div>
      <div class="card-stats"> <!--- Stats card right --->
          <div class="stats-bloc">
            <div class="balance">{{cardsBlock.balance}}</div>
            <div class="subtitle-stats">{{cardsBlock.subBalance}}</div>
          </div>
          <div class="stats-bloc">
            <div class="income">{{cardsBlock.income}}</div>
            <div class="subtitle-stats">{{cardsBlock.subIncome}}</div>
          </div>
          <div class="stats-bloc">
            <div class="outcome">{{cardsBlock.outcome}}</div>
            <div class="subtitle-stats">{{cardsBlock.subOutcome}}</div>
          </div>
          <div class="btn-desactivate">
            <!-- <i class="bi bi-toggle-off"></i> -->
            <div class="btn-ext">
              <div class="btn-int"></div>
            </div>
            <span class="subtitle-stats">{{cardsBlock.cardBtn}}</span>
          </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Cards',
  props: {
      data: {
          type: Array,
          required: true
      }
  }
}
</script>

<style scoped>
.content-card {
  margin-bottom: 15px;
  display: flex;
  height: 85%;
  justify-content: space-between;
}
.content-usercard {
  display: flex;
  width: 70%;
}
.arrow {
  display: flex;
  align-items: center;
  padding: 5px;
  margin-top: -10%;
  color: #197BBD;
}
i.fas {
  font-size: 20px;
}
.bar-card-right {
  border-left: 1px solid #E8E8E8;
  border-radius: 30px;
  height: 75%;
}
.top-info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 85%;
}
.card-user {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 100%;
  height: 75%;
  background: linear-gradient(180deg, #197BBD 0%, #3391D0 100%);
  border-radius: 26px;
  color: #ffffff;
}
.bot-info {
  height: 20%;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}
.card-account, .card-number, .bot-card {
  margin-left: 15px;
}
.card-number {
  display: flex;
  width: 70%;
  justify-content: space-between;
}
.bot-card {
  height: 17%;
}
.holder, .expire {
  display: flex;
  flex-direction: column;
}
.holder {
  width: 35%;
}
.stats-bot-card {
  font-weight: 200;
  font-size: 7.17776px;
  line-height: 9px;
}
.name-bot-card {
  font-weight: 300;
  font-size: 12.6167px;
  line-height: 13px;
}
.premium {
  font-style: normal;
  font-weight: 500;
  font-size: 8.11292px;
  line-height: 10px;
  color: rgba(255, 255, 255, 0.39);
  letter-spacing: -0.5px;
}
/* Stats card right */
.balance {
  color: #197BBD;
  font-size: 22px;
}
.income {
  color: #439A86;
}
.outcome {
  color: #BB4430;
}
.income, .outcome {
  font-size: 16px;
  line-height: 22px;
}
.balance {
  font-weight: bold;
}
.subtitle-stats {
  color: #AEAEAE;
  font-size: 12px;
  line-height: 17px;
}
.card-stats {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-end;
}
.card-stats, .btn-desactivate {
  text-align: end;
}
.btn-desactivate {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.btn-ext {
  background: #EBEBEB;
  border-radius: 13.617px;
  width: 33.69px;
  height: 16.45px;
  margin-bottom: 0.25em;
}
.btn-int {
  background: #CDCDCD;
  border-radius: 13.617px;
  width: 17.45px;
  height: 16.45px;
}
.btn-int, .btn-ext {
  align-self: flex-end;
} 
/* .bot-info {
  display: grid;
  grid-template-columns: 75% 35%;
} */
.stats-bar {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  font-size: 12px;
}
.limit-text {
  color: #AEAEAE;
  width: fit-content;
}
.weekly-numbers {
  font-weight: 600;
}
.bot-card {
  display: flex;
}
/* progressbar */
.progress { /* progress bar general */
  height: 9.47px;
  width: auto;
}
.progress-bar-card { /* progress bar travels filling */
  background: #197BBD;
  border-radius: 13.617px;
  width: 15%;
}
</style>
