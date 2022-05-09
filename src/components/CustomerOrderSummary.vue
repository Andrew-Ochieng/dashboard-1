<template>
    <div id="body">
        <div class=" md:mt-16 mt-8 mx-8 md:p-10 p-4 border-2 rounded-lg">
            <div>
                <h3 class="md:px-6 px-2 md:py-4 py-3 md:text-xl font-extrabold">Customer And Order Details</h3>
            </div>

            <table class="min-w-full">
                <thead v-bind:key="customer.id" v-for="customer in customer" class="border-b text-md text-gray-900 text-left">
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="md:px-6 px-2 md:py-4 py-3 md:text-md">Customer Name</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">{{customer.name}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="md:px-6 px-2 md:py-4 py-3 md:text-md">Phone Number</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">{{customer.number}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="md:px-6 px-2 md:py-4 py-3 md:text-md">Bag Option</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">{{customer.bagOpt}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="md:px-6 px-2 md:py-4 py-3 md:text-md">Type</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">{{customer.type}}</th>
                    </tr>
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="md:px-6 px-2 md:py-4 py-3 md:text-md">Note</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">{{customer.note}}</th>
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
                    name: 'Harun Hill',
                    number: '0700000000',
                    bagOpt: 'Nobag',
                    type: 'Delivery',
                    note: 'N/A'
                },
                   
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