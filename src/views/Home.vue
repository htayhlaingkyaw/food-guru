<template>
  <div class="container mt-4">
    <h1 class="text-center">Food Guru</h1>
    <ul
      class="list-unstyled"
      v-for="(restaurant, index) in restaurants"
      v-bind:key="index">
      <li>
        <img
          :src="require(`@/assets/restaurants/${restaurant.image}`)"
          class="img-fluid"/>
          <div class="restaurant-name">
            {{ restaurant.name }}
          </div>
          <div class="restaurant-description">
            <div class="text-muted mb-2">
              <span class="text-primary">$</span>$$, noodles, curry, asian
            </div>
            <div class="text-muted">
              <strong>No</strong> minimum | <strong>Free</strong>  Delivery
            </div>
          </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      restaurants: [
        {
          name: "Kyin Shin",
          image: "kyin-shin.jpg",
        },
        {
          name: "Shwe Khit",
          image: "shwe-khit.jpg",
        },
        {
          name: "Indian Tadka - Pyay Road",
          image: "indian-tadka-pyay-road.jpg",
        },
        {
          name: "Khine Thuka",
          image: "khine-thuka.jpg",
        },
        {
          name: "Fresh Kitchen",
          image: "fresh-kitchen.jpg",
        },
        {
          name: "My Way (Alone)",
          image: "my-way-alone.jpg",
        },
        {
          name: "Fresh Orange",
          image: "fresh-orange.jpg",
        },
      ],
    };
  },
};
</script>

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
