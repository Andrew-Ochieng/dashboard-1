<template>
    <div id="body">
        <div class="mt-8 md:p-8 p-4 border-2 rounded-lg w-full">
            <div>
                <h3 class="md:py-3 py-2 md:text-xl font-extrabold">Delivery Address</h3>
            </div>

            <table class="min-w-full">
                <thead v-bind:key="details.id" v-for="details in details" class="border-b text-md text-gray-900 text-left">
                    <tr class="border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm">
                        <th class="p-2 md:text-md">{{details.name}}</th>
                        <th class="p-2 text-right">{{details.address}}</th>
                    </tr>
                </thead>
            </table>
        </div>



    </div>
</template>

<script>
import AvatarOne from "../icons/avatar1.png"

    export default {
        name: 'ItemSummary',
        data(){
            return {
                details: [
                    {
                        name: 'Order Created',
                        address: '21, Brooklyn Road'
                    },
                    {
                        name: 'Building Name',
                        address: 'South NY Court'
                    },
                    {
                        name: 'Street',
                        address: '  Brooklyn Road'
                    },
                    {
                        name: 'Post Address',
                        address: '20206'
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