<template>
    <div id="body">
        <div class=" md:mt-16 mt-8 md:p-8 p-4 border-2 rounded-lg w-full">
            <table class="min-w-full">
                <thead class="border-b md:text-lg font-extrabold text-gray-900 text-left">
                    <tr class="">
                        <th class="md:px-6 px-2 md:py-4 py-3 md:text-xl text-lg">Items Summary</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">QTY</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">Price</th>
                        <th class="md:px-6 px-2 md:py-4 py-3">Total Price</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-bind:key="order.id" v-for="order in order" class="bg-white border-b transition duration-300 ease-in-out hover:bg-gray-100 text-sm text-gray-900 font-light">
                        <td class="md:px-6 px-2 md:py-4 py-3 whitespace-nowrap">
                            <div>
                                <img :src="`../icons/${order.icon}`" alt="">
                                <span>{{order.name}}</span>
                            </div>
                        </td>
                        <td class="md:px-6 px-2 md:py-4 py-3 whitespace-nowrap">{{order.qty}}</td>
                        <td class="md:px-6 px-2 md:py-4 py-3 whitespace-nowrap">{{order.price}}</td>
                        <td class="md:px-6 px-2 md:py-4 py-3 whitespace-nowrap">{{order.total}}</td>
                    </tr>
                </tbody>
            </table>
        </div>



       
    </div>
</template>

<script>
// import AvatarOne from "../icons/avatar1.png"
// import AvatarTwo from "../icons/avatar1.png"
// import AvatarThree from "../icons/avatar1.png"


    export default {
        name: 'ItemSummary',
        data(){
            return {
               order: [
                 {
                     icon: 'avatar1.png',
                     name: 'Milk',
                     qty: 'x1',
                     price: '$80',
                     total: '$80'
                 },
                 {
                     icon: 'avatar2.png',
                     name: 'Rice',
                     qty: 'x2',
                     price: '$120',
                     total: '$240'
                 },
                 {
                     icon: 'avatar3.png',
                     name: 'Sugar',
                     qty: 'x3',
                     price: '$100',
                     total: '$300'
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