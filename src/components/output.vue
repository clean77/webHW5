<template>
  <div id="app">
    <table>
      <thead>
      <tr>
        <th>Date</th>
        <th>Item</th>
        <th>Specifications</th>
        <th>Price</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="item in data">
        <td>{{ item.Date }}</td>
        <td>{{ item.Item }}</td>
        <td>{{ item.Specifications }}</td>
        <td>{{ item.Price }}</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "output"
}
</script>

<style scoped>
  body {
    padding: 40px;
    font: 14px "Lucida Grande", Helvetica, Arial, sans-serif;
  }

  table {
    width: 100%;
    border-collapse: collapse;
  }

  th {
    border: 1px solid #ddd;
    padding: 10px;
    text-align: left;
    background-color: #dc0201;
    color: white;
  }

  td {
    border: 1px solid #ddd;
    padding: 6px;
  }
</style>