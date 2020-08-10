<template>
  <div class="container mt-4">
    <h1>Food Guru</h1>
    <ul
      class="list-unstyled"
      v-for="(restaurant, index) in restaurants"
      v-bind:key="index"
    >
      <li><img :src="require(`@/assets/restaurants/${restaurant.image}`)" alt="" class="img-fluid"></li> 
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
