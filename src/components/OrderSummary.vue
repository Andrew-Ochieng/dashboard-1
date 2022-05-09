<template>
    <div id="body">
        <div class=" md:mt-16 mt-8 md:p-8 p-4 border-2 rounded-lg w-full">
            <div>
                <h3 class="md:py-3 py-2 md:text-xl font-extrabold">Order Summary</h3>
            </div>

            <table class="min-w-full">
                <thead v-bind:key="summary.id" v-for="summary in summary" class="border-b text-md text-gray-900 text-left">
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">{{summary.name}}</th>
                        <th class="p-2 text-right">{{summary.details}}</th>
                    </tr>
                </thead>
            </table>
        </div>

        <!--container2-->
        <div class="mt-8 md:p-8 p-4 border-2 rounded-lg">
            <table class="min-w-full">
                <thead v-bind:key="total.id" v-for="total in total" class="text-md text-gray-900 text-left font-extrabold">
                    <tr class="transition duration-300 ease-in-out hover:bg-gray-100">
                        <th class="p-2 md:text-md">{{total.name}}</th>
                        <th class="p-2 text-right">{{total.details}}</th>
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
                summary: [
                    {
                        name: 'Order Created',
                        details: 'Mon, May 9, 2022'
                    },
                    {
                        name: 'Order Time',
                        details: '09.30AM'
                    },
                    {
                        name: 'Subtotal',
                        details: '$450'
                    },
                    {
                        name: 'Delivery Fee',
                        details: '$0.00'
                    }
                ],

                total: [
                    {
                    name: 'Total',
                    details: '$900'
                }
                ]
            }
        }
    }
</script>

<style scoped>


</style>