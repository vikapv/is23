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
     <input type="text" class="form-control" id="date" >
     </div>
     <div class="mb-3">
      <label for="quantily" class="form-label">Количество</label>
     <input type="text" class="form-control" id="quantily" >
     </div>
     <div class="mb-3">
      <label for="priced" class="form-label">Цена за единицу товара</label>
     <input type="text" class="form-control" id="prised" >
     </div>
     <button type="button" class="btn btn-light">Добавить</button>
   </form>
    </div>
  </div>
</div>

</template>


