<template>
    <tr>
        <td style="border: 1px solid black"> {{ data[0] }} </td>
        <td style="border: 1px solid black"> {{ data[1] }} </td>
        <td style="border: 1px solid black"> {{ data[2] }} </td>
        <td style="border: 1px solid black"> {{ data[3] }} </td>
        <td style="border: 1px solid black"> {{ data[4] }} </td>
        <td style="border: 1px solid black"> {{ data[5] }} </td>
        <td style="border: 1px solid black"> {{ data[6] }} </td>
    </tr>
</template>

<script>
export default {
    name: "Row",
    props: ['data']
}
</script>

<style>

</style>
