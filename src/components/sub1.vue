<template>
    <div>
        sub
        <table border=1>
            <tr v-for="item in exampleProp" :key="item.e">
                <td>{{item.e}}</td>
                <td>{{item.k}}</td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {
    name: "sub1",
    props: ['exampleProp'],
    data() {
      return {

      }  
    },
    computed: {
        test: function() {
            return this.exampleProp
        }
    }
}
</script>

<style>
</style>
