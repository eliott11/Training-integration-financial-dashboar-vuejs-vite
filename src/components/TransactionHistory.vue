<template>
    <section class="transactionhistory block-shadow">
        <h4>Transaction History</h4>
        <table>
            <thead>
                <tr>
                    <th>Reciever</th>
                    <th>Type</th>
                    <th>Date</th>
                    <th class="amountTitle">Amount</th>
                </tr>
            </thead>
            <tbody v-for="(transacTableBlock, index) in data" :key="index">
                <tr>
                    <td><div class="name-trans"><i :class="`${transacTableBlock.logoLib} ${transacTableBlock.logo}`"></i>{{transacTableBlock.nameReciever}}</div></td>
                    <td class="type-name">{{transacTableBlock.type}}</td>
                    <td class="date">{{transacTableBlock.date}}</td>
                    <td class="amount">{{transacTableBlock.amount}}$</td>
                </tr>
            </tbody>
        </table>
    </section>
</template>

<script>
export default {
  name: 'TransactionHistory',
  props: {
      data: {
          type: Array,
          required: true
      }
  }
}
</script>

<style scoped>
table { /* table */
    width:-webkit-fill-available;
    height: 85%;
}
th { /* head table */
    text-align: start;
    font-weight: lighter;
    margin: 10px;
    color: #AEAEAE;
}
tbody { /* body table */
    font-weight: normal;
    font-size: 12px;
}
td { /* line bottom */
    border-bottom: 0.5px solid #ECECEC; /* à appliquer sur le TR pr faire une ligne entière mais veut pas (à résoudre)*/
    inline-size: 10px;

}
td[class*="name-trans"] { /* center content except name-trans */
    display: flex;
    align-items: center;
}
i { /* icons */
    margin-right: 10px;
    background-color: #EFEFEF;
    border-radius: 5px;
    padding: 3px;
}
.name-trans { /* icons & name row */
    display: flex;
    flex-direction: row;
    align-items: center;
}
.bi-cart, .bi-truck, .fa-feather, .bi-person, .bi-person { /* icons */
  display: flex;
  align-items: center;
}
.name-trans, .amount { /* title row & price */
    color: #404040;
}
.type-name, .date { /* type & date */
    color: #C7C7C7;
    margin: 5px 10px;
    font-weight: 300;
}
.amountTitle ,.amount { /* price */
    text-align: end;
}
.amount { /* price */
    font-weight: bold;
}
</style>
