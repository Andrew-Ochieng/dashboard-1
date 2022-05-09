<template>
  <div class="md:flex md:gap-32 justify-center md:mx-16 mx-8">
    <div class="md:selection:mx-4">
      <ItemSummary />
      <CustomerOrderSummary />
    </div>
    <aside class="align-right md:mx-8">
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