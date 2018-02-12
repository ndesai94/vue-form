<template>
    <div>
        <table style="border: 1px solid black">
            <thead>
                <tr>
                    <th style="border: 1px solid black">Prefix</th>
                    <th style="border: 1px solid black">First Name</th>
                    <th style="border: 1px solid black">Last Name</th>
                    <th style="border: 1px solid black">Street</th>
                    <th style="border: 1px solid black">City</th>
                    <th style="border: 1px solid black">State</th>
                    <th style="border: 1px solid black">Zip Code</th>
                </tr>
            </thead>
            <tbody>
                <Row v-for="(row, index) in rows" v-bind:data="row" v-bind:key="index"></Row> 
            </tbody>
            
        </table>
    </div>
</template>

<script>
import Row from './Row'

export default {
    name: "Table",
    components: {
        Row
    },
    props: ['rows']
}
</script>

<style>

</style>
