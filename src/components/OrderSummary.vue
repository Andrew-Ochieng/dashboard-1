<template>
    <div id="body">
        <div class=" md:mt-16 mt-8 mx-8 md:p-10 p-4 border-2 rounded-lg">
            <div>
                <h3 class="md:py-3 py-2 md:text-xl font-extrabold">Order Summary</h3>
            </div>

            <table class="min-w-full">
                <thead v-bind:key="orderSummary.id" v-for="orderSummary in orderSummary" class="border-b text-md text-gray-900 text-left">
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">Order Created</th>
                        <th class="p-2 text-right">{{orderSummary.created}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">Order Time</th>
                        <th class="p-2 text-right">{{orderSummary.time}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">SubTotal</th>
                        <th class="p-2 text-right">{{orderSummary.subtotal}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">Delivery Fee</th>
                        <th class="p-2 text-right">{{orderSummary.deliveryFee}}</th>
                    </tr>
                </thead>
            </table>
        </div>
        <!--container2-->
        <div class="mt-8 mx-8 md:p-10 p-4 border-2 rounded-lg">
            <table class="min-w-full">
                <thead v-bind:key="orderSummary.id" v-for="orderSummary in orderSummary" class="text-md text-gray-900 text-left font-extrabold">
                    <tr class="transition duration-300 ease-in-out hover:bg-gray-100">
                        <th class="p-2 md:text-md">Total</th>
                        <th class="p-2 text-right">{{orderSummary.total}}</th>
                    </tr>
                </thead>
            </table>
        </div>


    </div>
</template>

<script>
import avatar1 from "../icons/avatar1.png"

    export default {
        name: 'ItemSummary',
        data(){
            return {
               orderSummary: [
                 {
                    created: 'Mon, May 9, 2022',
                    time: '09.30AM',
                    subtotal: '$450',
                    deliveryFee: '$0.00',
                    total: '$800'
                 }
                   
               ] 
            }
        }
    }
</script>

<style scoped>
/* #body {
    font-family: 'Poppins', sans-serif;
    background-color: rgba(92, 161, 182, 0.384);
} */

</style>