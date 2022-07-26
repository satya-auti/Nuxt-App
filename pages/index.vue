<template>
  <div>
    
    <h1 v-if="userData.show" :style="{color: userData.mycolor}">Hello Nuxt Js</h1>
    <nuxt-demo></nuxt-demo>
    <hr>
    <div>
        <table>
            <tr>
                <td>
                    <label class="text-red-600" for="firstName">First Name</label>
                </td>
                <td>
                    <input type="text" v-model="userData.firstName" name="firstName" id="firstName" placeholder="First Name"><br/>
                </td>
            </tr>
            <tr>
                <td>
                    <label for="lastName">Last Name</label>
                </td>
                <td>
                    <input  type="text" v-model="userData.lastName" name="lastName" id="lastName" placeholder="Last Name">
                </td>
            </tr>
            <tr>
                <td>
                    <label for="email"> Email </label>
                </td>
                <td>
                     <input  type="email" v-model="userData.email" name="email" id="email" placeholder="Email">    
                </td>
            </tr>

            <tr>
                <td>

                </td>
                <td>

                </td>
            </tr>

            <tr>
                <td>
                    <input type="color" v-model="userData.mycolor">
                </td>
                <td>
                    <button class="rounded-xl bg-black text-white" type="submit" >Submit</button> &nbsp;
                    <button class="rounded-xl bg-black text-white" type="reset" >Reset</button>
                </td>
            </tr>
        </table>

        <hr>

        <table>
            <tr>
                <th>
                    Full Name
                </th>
                <th>
                    Email
                </th>
                <th>

                </th>
            </tr>
            <tr>
                <td>
                   <h1 v-if="userData.show" :style="{color: userData.mycolor}">{{userData.fullName}}</h1>
                </td>
                <td v-if="userData.show" :style="{color: userData.mycolor}">
                    {{userData.email}}
                </td>
            </tr>
            <tr>
                <td>
                    
                </td>
                <td>
                   
                </td>
            </tr>

            <tr>
                <td>

                </td>
                <td>
                        
                </td>
            </tr>
        </table>
        
        

        
        
    </div>
  </div>
</template>

<script setup lang="ts">
import NuxtDemo from '~/components/nuxt-demo.vue';
//  exports default 
// export default {
//         // name:'App',
//         data(){
//             return {};
//         },
//     };

definePageMeta({
    components: { 
        NuxtDemo 
    }
});

let userData = reactive({
    firstName : 'Satya',
    lastName : 'Auti',
    fullName : computed(() =>{
        return userData.firstName +' '+ userData.lastName;
    }),
    email : 'auti.satyavan3@gmail.com',
    mycolor : '#00FF00',
    show : true,
})


</script>


<style scoped>

</style>
