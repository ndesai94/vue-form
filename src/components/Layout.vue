<template>
    <div>
        <h2>{{ myTitle }}</h2> <br /> <br />
        <Form @newRow="addRow"></Form> <br /> <br /> <br /> <br />
        <Table :rows="rows"></Table>
    </div>
</template>

<script>
import Form from './Form'
import Table from './Table'

export default {
  name: "Layout",
  components: {
      Form, Table
  },
  props: ["myTitle"],
  data() {
    return {
      rows: [
        {
          allRows: Array(7).fill(null)
        }
      ]
    };
  },
  methods: {
    addRow(data) {
      this.rows.push([
        data[0],
        data[1],
        data[2],
        data[3],
        data[4],
        data[5],
        data[6]
      ]);
    }
  }
};
</script>

<style>

</style>
