<script setup>

</script>

<template>
<div class = "container">
  <div class="row">
    <div class="col">
      <h1 class="text-center">Учет товаров</h1>
   <form action="">
    <div class="mb-3">
      <label for="name" class="form-label">Название товара</label>
     <input type="text" class="form-control" id="name" >
     </div>
     <div class="mb-3">
      <label for="date" class="form-label">Дата приема товара</label>
     <input type="date" class="form-control" id="date" >
     </div>
     <div class="mb-3">
      <label for="count" class="form-label">Количество</label>
     <input type="number" class="form-control" id="count" >
     </div>
     <div class="mb-3">
      <label for="priced" class="form-label">Цена за единицу товара</label>
     <input type="number" class="form-control" id="prised" >
     </div>
     <div class="text-center mb-3">
      <button type="button" class="btn btn-light">Добавить</button>
     </div>

   </form>
    </div>
  </div>
</div>

<div class="row row-cols-1 row-cols-md-3 g-4">
  <div class="col">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">iphone</h5>
        <p class="card-text">25.11.24</p>
        <p class="card-text">$200 </p>
        <p class="card-text"> 5 шт </p>
        <div class = "card-footer">
          <button class="btn btn-outline-danger"> Удалить</button>
        </div>
      </div>
    </div>
    </div>
  </div>

  <div class="row my-4">
    <div class="col">
      <h3 class="text-end">Общая сумма: $45854</h3>
    </div>
  </div>

</template>


