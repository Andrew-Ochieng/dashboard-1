<template>
  <div class="md:flex gap-8">
    <div>
      <ItemSummary />
      <CustomerOrderSummary />
    </div>
    <aside class="align-right">
      <OrderSummary />
      <DeliveryAddress />
    </aside>

  </div>
</template>

<script>
import ItemSummary from "./components/ItemSummary.vue"
import OrderSummary from "./components/OrderSummary.vue"
import CustomerOrderSummary from "./components/CustomerOrderSummary.vue"
import DeliveryAddress from "./components/DeliveryAddress.vue"

  export default {
    name: 'App',
    components: {
      ItemSummary,
      OrderSummary,
      CustomerOrderSummary,
      DeliveryAddress
    }
  }
</script>

<style scoped>
* {
  /* background-color: rgba(92, 161, 182, 0.384); */
  font-family: 'Poppins', sans-serif;
}


</style>