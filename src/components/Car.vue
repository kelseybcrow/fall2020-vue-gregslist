<template>
  <div class="col-4 car">
    <router-link :to="{name: 'CarDetails', params: { id: carData._id}}">
      <div class="card">
        <img class="card-img-top" :src="carData.imgUrl" alt />
        <div class="card-body">
          <h4 class="card-title">{{carData.make}} - {{carData.model}} - {{carData.year}}</h4>
        </div>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "Car",
  props: {
    carData: {
      type: Object,
      required: true
    }
  },
  methods: {

  },
}
</script>

<style scoped>
.car {
  transition: 0.5s ease;
  cursor: pointer;
}
.car:hover {
  transform: scale(1.05);
}
</style>