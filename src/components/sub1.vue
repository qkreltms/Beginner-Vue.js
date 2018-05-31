<template>
    <div>
        sub
        <!-- <table border=1>
            <tr v-for="item in exampleProp" :key="item.e">
                <td>{{item.e}}</td>
                <td>{{item.k}}</td>
            </tr>
        </table> -->
        <ul>
            <li v-for="item in exampleProp">{{item}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'sub1',
    props: ['exampleProp'],
    data() {
      return {

      }  
    },
    computed: {
    }
}
</script>

<style>
</style>
