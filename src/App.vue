<template>
  <div id="app">
    <router-view/>
  </div>
</template>


<style>
.restaurant-name {
    font-weight: 700;
    margin-top: 15px;
}

.restaurant-description {
    font-size: 0.9rem;
}

.list-unstyled>li {
    cursor: pointer;
}

.banner {
    height: 250px;
}

.name,.price {
    font-weight: 700;
    font-size: 0.9rem;
}
</style>