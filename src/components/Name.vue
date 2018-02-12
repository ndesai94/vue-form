<template>
    <div>
        <h3>Your Full Name:</h3> <br />
        <select @input="updatePrefix($event.target.value)">
            <option disabled selected value> -- </option>
            <option value="mr">Mr.</option>
            <option value="mrs">Mrs.</option>
            <option value="ms">Ms.</option>
        </select>
        <input type="text" @input="updateFirst($event.target.value)"/>
        <input type="text" @input="updateLast($event.target.value)"/>
        <br /><br />
    </div>
</template>

<script>
export default {
    name: "Name",
    methods: {
        updatePrefix: function (value) {
            this.$emit('prefix', value);
        },
        updateFirst: function (value) {
            this.$emit('first', value);
        },
        updateLast: function (value) {
            this.$emit('last', value);
        }
    }
}
</script>

<style>

</style>
