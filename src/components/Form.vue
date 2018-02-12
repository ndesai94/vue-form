<template>
    <div>
        <Name @prefix="updatePrefix" @first="updateFirst" @last="updateLast"></Name>
        <Address @street="updateStreet" @city="updateCity" @state="updateState" @zip="updateZip"></Address>
        <br /> <br >
        <button @click="addRow">Add Record</button>
    </div>
</template>

<script>
import Name from './Name'
import Address from './Address'

export default {
    name: "Form",
    components: {
        Name, Address
    },
    data() {
        return {
            prefix: null,
            first: null,
            last: null,
            street: null,
            city: null, 
            state: null,
            zip: null
        }
    },
    methods: {
        updatePrefix(data) {
            this.prefix = data;
        },
        updateFirst(data) {
            this.first = data;
        },
        updateLast(data) {
            this.last = data;
        },
        updateStreet(data) {
            this.street = data;
        },
        updateCity(data) {
            this.city = data;
        },
        updateState(data) {
            this.state = data;
        },
        updateZip(data) {
            this.zip = data;
        },
        addRow(data) {
            this.$emit('newRow', [this.prefix, this.first, this.last, this.street, this.city, this.state, this.zip]);
        }
    }
}
</script>

<style>

</style>
