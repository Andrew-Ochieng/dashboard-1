<template>
    <div id="body">
        <div class=" md:mt-16 mt-8 md:p-10 p-4 border-2 rounded-lg">
            <div>
                <h3 class="md:px-6 px-2 md:py-4 py-3 md:text-xl font-extrabold">Customer And Order Details</h3>
            </div>

            <table class="min-w-full">
                <thead v-bind:key="customer.id" v-for="customer in customer" class="border-b text-md text-gray-900 text-left">
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="md:px-6 px-2 md:py-4 py-3 md:text-md">{{customer.name}}</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">{{customer.details}}</th>
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
               customer: [
                   {
                       name: 'Customer Name',
                       details: 'Harun Hill'
                   },
                   {
                       name: 'Phone Number',
                       details: '+2547 0123 4567'
                   },
                   {
                       name: 'Bag Option',
                       details: 'No bag'
                   },
                   {
                       name: 'Type',
                       details: 'Delivery'
                   },
                   {
                       name: 'Note',
                       details: 'N/A'
                   }
               ] 
            }
        }
    }
</script>

<style scoped>




</style>