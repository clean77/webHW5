<template>
  <form v-on:submit.prevent="addItem">
    <div>
      <label for="Date">日期</label>
      <input type="date" id="Date" name="Date" v-model="itemDate">
      <label for="Item">品項</label>
      <input type="text" id="Item" name="Item" v-model="itemItem">
      <label for="Specifications">規格</label>
      <input type="text" id="Specifications" name="Specifications" v-model="itemSpecification">
      <label for="Price">價錢(元/公斤)</label>
      <input type="text" onkeyup="value=value.replace(/[^\d.]/g,'')" id="Price" name="Price" v-model="itemPrice">
      <button type="submit">Submit</button>
    </div>

  </form>

</template>

<script>
export default {
  data() {
    return {
      itemDate: null,
      itemItem: null,
      itemSpecification: null,
      itemPrice: null
    }
  },
  methods: {
    addItem(){
      let item = {
        date: this.itemDate,
        item: this.itemItem,
        specification: this.itemSpecification,
        price: this.itemPrice
      }
      itemDate: null
      itemItem: null
      itemSpecification: null
      itemPrice: null
    }
  }
}
</script>

<style scoped>
  body {
    padding: 40px;
    font: 14px "Lucida Grande", Helvetica, Arial, sans-serif;
  }

  div {
    display: flex;
    flex-direction: column;
    /*水平置中*/
    justify-content: center;
    /* 垂直置中 */
    align-items: center;
  }

  label {
    display: flex;
    justify-content:flex-start;
    width:30%;
    /*display: block;*/
    margin-top: 5px;
    margin-bottom: 5px;
  }

  input{
    outline-style: none;
    border: 1px solid #ccc;
    border-radius: 3px;
    height: 27px;
    width: 30%;
    margin-bottom: 8px;
    box-sizing: border-box;
  }

  input:focus{
    border-color: #66afe9;
    outline: 0;
    box-shadow: inset 0 1px 1px rgba(163, 231, 241, 0.76),0 0 6px rgba(163, 231, 241, 0.76);
    border-radius: 3px;
  }

  button{
    font-size: 15px;
    color: white;
    background: #dc0201;
    border: 0;
    border-radius: 3px;
    height: 32px;
    width: 110px;
    margin-top: 7px;
    margin-bottom: 17px;
  }
</style>