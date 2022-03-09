<script>
import Menu from './components/Menu.vue'
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import './assets/index.scss'

export default {
  name: 'App',
  components: {
    Menu,
    Header,
    Content
  },
  data() {
    return {
      menuData: [
        {
          titleLogo: "cloudcash",
          logoLib: "bi",
          logoLib2: "fas",
          logo1: "graph-up",
          logo2: "list-ul",
          logo3: "credit-card",
          logo4: "file-earmark",
          logo5: "bookmark-star",
          logo6: "gear",
          name1: "Overview",
          name2: "Transactions",
          name3: "Cards",
          name4: "Invoices",
          name5: "Goals",
          name6: "Settings",
          p1: "Give your money",
          p2: "awesome space in cloud",
          textBtn: "Upgrade to premium ",
          logoBtn: "fa-arrow-up"
        },
      ],
      headerData: [
        {
          h3: "Weekly sumup",
          h6: "Get summary of your weekly online transactions here.",
          logoLib: "bi",
          logo1: "envelope-fill",
          logo2: "bell-fill",
          logo3: "person-circle",
          p1: "Eliott",
          p2: "Admin Account",
          textBtn: "Upgrade to premium ",
          logoBtn: "arrow-up-circle"
        },
      ],
    }
  }
}
</script>

<template>
  <div class="page"> <!--- page including all contents --->
    <Menu :data="menuData"/>
    <div class="margin-content"> <!--- content --->
      <Header :data="headerData"/>
      <Content />
    </div>
  </div>
</template>

<style scoped>
.page { /* display page */
  display: flex;
  /* max-height: 100vh;
  overflow: auto; */
}
.margin-content { /* margin content */
  padding: 0 30px 0 28px;
  flex-grow:1;
}
</style>
