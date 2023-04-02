<template>
  <div class="card">
    <img :src="image" alt="" />
    <h2>{{ name }}</h2>
    <p>{{ price }}</p>
    <button @click="$emit('add')" class="addCart">add to cart</button>
  </div>
</template>

<script>
export default {
  components: {},
  props: {
    name: String,
    image: String,
    price: String,
  },
};
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  width: 25rem;
  height: 25rem;
  margin: 4rem;
  color: #151515;
}
.card:hover .addCart {
  display: block;
}

p {
  margin-top: 0rem;
  font-size: 1.5rem;
}
img {
  width: 20rem;
  height: 20rem;
  object-fit: cover;
}
.addCart {
  margin-top: 28.5rem;
  position: absolute;
  width: 11rem;
  height: 2.5rem;
  border: none;
  border-radius: 0.2rem;
  background-color: #04361f;
  color: #fff;
  font-size: 1.3rem;
  opacity: 0.7;
  transition: 0.3s;
}
.addCart:hover {
  cursor: pointer;
  opacity: 0.8;
}

.addCart:active {
  transform: scale(0.9);
}
</style>
