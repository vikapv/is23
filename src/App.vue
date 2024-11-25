<script setup>
import {ref,computed} from "vue";

const products = ref ([
  {
id:1 ,
name: 'Iphone',
date: '20.11.2024',
count: 100,
price: 1500,
},
{
  id:2 ,
name: 'Sumsung',
date: '21.11.2024',
count: 95,
price: 1600,
},
{
  id:3 ,
name: 'Poco',
date: '23.11.2024',
count: 90,
price: 1500,
},
{id:4 ,
name: 'Xiaomi',
date: '27.11.2024',
count: 100,
price: 1400,
}])
const name = ref('');
const date = ref('');
const count = ref(1);
const price = ref(0);

const addProduct = () => {
  if (name.value && date.value && count.value && price.value){
    products.value.push(
      {
        id: Date.now(),
        name: name.value,
        date: (new Date(date.value)).toLocaleDateString(),
        count: count.value,
        price: price.value,
      }
    );
  }
}

const removeProduct =(id) => {
  products.value = products.value.filter((product) => product.id !=id);
}

const totalSum = computed(() =>{
  return products.value.reduce((sum,product) => sum + (product.price * product.count),0)
});
</script>

<template>
<div class = "container">
  <div class="row">
    <div class="col">
      <h1 class="text-center">Учет товаров</h1>
   <form>
    <div class="mb-3">
      <label for="name" class="form-label">Название товара</label>
     <input type="text" v-model="name" class="form-control" id="name" >
     </div>
     <div class="mb-3">
      <label for="date" class="form-label">Дата приема товара</label>
     <input type="date" v-model=" date" class="form-control" id="date" >
     </div>
     <div class="mb-3">
      <label for="count" class="form-label">Количество</label>
     <input type="number" v-model="count" class="form-control" id="count" >
     </div>
     <div class="mb-3">
      <label for="priced" class="form-label">Цена за единицу товара</label>
     <input type="number" v-model="price" class="form-control" id="prised" >
     </div>
     <div class="text-center mb-3">
      <button  type="button" @click="addProduct" class="btn btn-light">Добавить</button>

     </div>

   </form>
    </div>
  </div>



        <div class="row row-cols-md-3 g-4">
   <div class="col" v-for="product in products" :key="product.id">
    <div class="card h-100">
      <div class="card-body">
       <h5 class="card-title">{{ product.name }}</h5>
       <p class="card-text">{{ product.date }}</p>
       <p class="card-text">{{ product.price }}</p>
       <p class="card-text">{{ product.count}}</p>
      </div>
        <div class = "card-footer">
          <button @click="removeProduct(product.id)" class="btn btn-outline-danger"> Удалить</button>
        </div>
      </div>
    </div>
  </div>
  <div class="row my-4">
    <div class="col">
      <h3 class="text-end">Общая сумма: {{ totalSum }}  </h3>
    </div>
  </div>


</div>

</template>


