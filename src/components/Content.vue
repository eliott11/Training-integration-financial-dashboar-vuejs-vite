<script>
import Cards from './Cards.vue'
import TransactionHistory from './TransactionHistory.vue'
import Pricing from './Pricing.vue'
import Stats from './Stats.vue'
import NewTransaction from './NewTransaction.vue'

export default {
  name: 'Content',
  components: {
    Cards,
    TransactionHistory,
    Pricing,
    Stats,
    NewTransaction
  },
  data() {
    return {
      cardsData: {
        logoLib: "fas",
        logo: "fa-chevron",
        logoLeft: "left",
        logoRight: "right",
        namecard: "cloudcash",
        statusAccount: "PREMIUM ACCOUNT",
        numbercards1: "5789",
        numbercards2: "****",
        numbercards3: "****",
        numbercards4: "2847",
        cardHolder: "Card Holder",
        nameHolder: "Mike Smith",
        expireDate: "Expire date",
        date: "06/21",
        weeklySpendTitle: "Weekly payment limit",
        weeklySpendAmount: "$350.60 / $4000",
        balance: "$ 2850.75",
        subBalance: "Current Balance",
        income: "$ 1500.50",
        subIncome: "Income",
        outcome: "$ 350.60",
        subOutcome: "Outcome",
        cardBtn: "Deactivate Card"
      },
      transactionHistoryTableData: [
        {
          logoLib: "bi",
          logo: "bi-cart",
          nameReciever: "Tesco Market",
          type: "Shopping",
          date: "13 Dec 2020",
          amount: "75.67"
        },
        {
          logoLib: "bi",
          logo: "bi-truck",
          nameReciever: "ElectroMen Market",
          type: "Shopping",
          date: "14 Dec 2020",
          amount: "250.00"
        },
        {
          logoLib: "fas",
          logo: "fa-feather",
          nameReciever: "Fiorgo Restaurant",
          type: "Food",
          date: "7 Dec 2020",
          amount: "19.50"
        },
        {
          logoLib: "bi",
          logo: "bi-person",
          nameReciever: "John Matthew Kayne",
          type: "Sport",
          date: "6 Dec 2020",
          amount: "350"
        },
        {
          logoLib: "bi",
          logo: "bi-person",
          nameReciever: "Ann Marlin",
          type: "Shopping",
          date: "31 Nov 2020",
          amount: "430"
        },
      ],
      pricingData: [
        {
          price: "550",
          date: "12/20/20",
          logoLib: "fa",
          logo: "mountain",
          label: "Holidays"
        },
        {
          price: "200",
          date: "12/20/20",
          logoLib: "fa",
          logo: "brush",
          label: "Rent"
        },
        {
          price: "820",
          date: "12/20/20",
          logoLib: "bi",
          logo: "controller",
          label: "Games"
        },
      ],
      statsData: [
        {
          logoLib: "bi",
          logo: "cart",
          progressbarClass: "shopping",
          statsPourcent: "52",
          titleStats: "Shopping"
        },
        {
          logoLib: "bi",
          logo: "truck",
          progressbarClass: "electro",
          statsPourcent: "21",
          titleStats: "Electronics"
        },
        {
          logoLib: "fa",
          logo: "plane",
          progressbarClass: "travels",
          statsPourcent: "74",
          titleStats: "Travels"
        },
      ],
      newTransacData: [
        {
          h4: "New Transaction",
          logoLib1: "bi",
          logo1: "plus-circle-fill",
          namePerson1: "Ann",
          namePerson2: "Monica",
          namePerson3: "John",
          namePerson4: "Mike",
          namePerson5: "Mia",
          addNew: "Add New",
          textBtn: "Send the transfert ",
          logoLib2: "fab",
          logo2: "fa-bitcoin",
          pClass: "text-btn-right",
          classImg1: "btc1",
          classImg2: "btc2",
          logoLib3: "fa",
          pClass2: "fa-chevron-right",
          p1: "Get great",
          p2: "loan!"
        },
      ]
    }
  }
}
</script>

<template>
  <div class="pagecontent"> <!--- page --->
    <div class="content-pagecontent"> <!--- content --->
      <div class="content-left"> <!--- content left --->
        <Cards class="cards-content" :data="cardsData"/>
        <TransactionHistory class="transhisto-content" :data="transactionHistoryTableData"/>
      </div>
      <div class="content-right"> <!--- content right --->
        <Pricing class="pricing-content" :data="pricingData"/>
        <Stats class="stats-content" :data="statsData"/>
        <NewTransaction class="newtransac-content" :data="newTransacData"/>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .pagecontent { /* general content */
    display: flex;
    flex-direction: column;
    margin-top: 10px;
  }
  .content-pagecontent { /* content in page */
    display: flex;
  }
  .content-left {  /* content left */
    width: 50%;
    height: 85vh;
    display: flex;
    float: left;
    flex-direction: column;
    justify-content: space-between;
    margin-right: 5px;
  }
  .cards-content, .transhisto-content { /* content left height */
    height: 49%;
  }
  .pricing-content, .stats-content { /* content right height */
    height: 35%;
  }
  .newtransac-content { /* content right height */
    height: 30%;
  }
  .content-right { /* content right display & width */
    width: 50%;
    display: flex;
    float: right;
    flex-direction: column;
    justify-content: space-between;
  }
</style>