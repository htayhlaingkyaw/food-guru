<template>
  <div class="container mt-4">
    <h1 class="text-center">
      <router-link to="/">FoodGuru</router-link>
    </h1>

    <div class="container-fluid px-0">
      <img
        :src="require(`@/assets/restaurants/${restaurant.image}`)"
        class="img-fluid"/>
    </div>

    <div class="card rounded-0 shadow-sm">
      <div class="card-body">
        <div class="restarant-name">
          {{ restaurant.name }}
        </div>

        <div class="restaurant-description">
          <div class="text-muted mb-2">
            <span class="text-primary">$</span>$$ noodles, curry, asian
          </div>
        </div>
      </div>
    </div>

    <div class="card px-0 rounded-0 mt-4">
      <div class="card-body">
        <div class="item" v-for="(item, index) in restaurant.items" v-bind:key="index">
          <div class="name">{{ item.name }}</div>
          <div class="price mt-3">MMK {{ item.price }}</div>
          <hr />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      restaurant: {
        name: "Kyin Shin",
        image: "kyin-shin.jpg",
        items: [
          {
            name: "Shan Noodle",
            price: 1500,
          },
          {
            name: "Hot Tofu Noodle",
            price: 1500,
          },
          {
            name: "Fired Tofu Noodle",
            price: 1500,
          },
          {
            name: "Nhin Htoke",
            price: 1500,
          },
          {
            name: "Pord Head Salad",
            price: 2000,
          },
        ],
      },
    };
  },
};
</script>
