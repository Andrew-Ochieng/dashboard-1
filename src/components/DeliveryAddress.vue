<template>
    <div id="body">
        <div class="mt-8 mx-8 md:p-6 p-3 border-2 rounded-lg">
            <div>
                <h3 class="md:py-3 py-2 md:text-xl font-extrabold">Delivery Address</h3>
            </div>

            <table class="min-w-full">
                <thead v-bind:key="address.id" v-for="address in address" class="border-b text-md text-gray-900 text-left">
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">Order Created</th>
                        <th class="p-2 text-right">{{address.line}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">Building Name</th>
                        <th class="p-2 text-right">{{address.building}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">Street</th>
                        <th class="p-2 text-right">{{address.street}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">Postcode Address</th>
                        <th class="p-2 text-right">{{address.postcode}}</th>
                    </tr>
                </thead>
            </table>
        </div>
    <!-- <OrderSummary v-bind:address="addresss"/> -->



    </div>
</template>

<script>
import AvatarOne from "../icons/avatar1.png"

    export default {
        name: 'ItemSummary',
        data(){
            return {
               address: [
                 {
                    line: '12, Brooklyn Road',
                    building: 'James Brown Court',
                    street: 'Brooklyn Road',
                    postcode: '30306'
                 }
                   
               ],
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