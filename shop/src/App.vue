
<template>
 <table>
        <thead>
            <th>Название</th>
            <th>Цена</th>
            <th></th>
        </thead>

        <tbody>
            <tr v-for="item in items" :key="item.id">
                <td v-text="item.title"></td>

                <td>${{ item.price.toFixed(2) }}</td>

                <button v-on:click="modalIOpen"> Добавить в корзину </button>
            </tr>
        </tbody>
    </table>

   
    <div class="modal" v-if="isModaIOpened"></div>
    <button v-on:click="modalClose">Закрыть корзину </button>
</template>
<script>



export default{
  data() {
    return{
      items: [
    {id:1,
    title:"Jacket white",
    price:336},
    {id:2,
    title:"Hat red",
    price:116},
    {id:3,
    title:"Socks orange",
    price:970},
    {id:4,
    title:"Jacket white",
    price:386},
    {id:5,
    title:"Shirt black",
    price:262},
    {id:6,
    title:"Jacket white",
    price:482},
    {id:7,
    title:"Shoes black",
    price:237},
    {id:8,
    title:"Hat orange",
    price:570},
    {id:9,
    title:"Hat green",
    price:279},
    {id:10,
    title:"Shirt orange",
    price:441},
    {id:11,
    title:"Hat white",
    price:778},
    {id:12,
    title:"Hat white",
    price:938},
    {"id":13,
    title:"Shirt red",
    price:145},
    {id:14,
    title:"Jacket green",
    price:730},
        {id:15,
        title:"Jacket black",
        price:234},
        {id:16,
        title:"Hat black",
        price:667},
        {id:17,
        title:"Hat white",
        price:675},

        {id:18,
        title:"Hat orange",
        price:574},
        
        {id:19,
        title:"Hat red",
        price:558},

        {id:20,
        title:"Hat orange",
        price:382},
      ],
      isModaIOpened: false,
      
    }
  },
  methods:{
    modalIOpen(){
      this.isModaIOpened = true;
    },
    modalClose(){
      this.isModaIOpened = false;
    }
  }

};
 

</script>

<style lang="scss">
.modal{
  border: 1px solid red;
  width: 500px;
  height: 400px;
  
  
}
</style>