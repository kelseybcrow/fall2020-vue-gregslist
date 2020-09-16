<template>
  <div id="car-details" class="container">
    <div class="row pt-3" v-if="car._id">
      <div class="col-6">
        <h2>{{car.make}} - {{car.model}} - {{car.year}}</h2>
        <p>${{car.price.toFixed(2)}}</p>
        <h4>{{car.description}}</h4>
        <div class="d-flex justify-content-between">
          <button class="btn btn-outline-danger" @click="deleteCar">Delete</button>
          <button class="btn btn-outline-info" @click="bid">+ $100</button>
        </div>
      </div>
      <div class="col-6">
        <img class="card-img-top" :src="car.imgUrl" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Car-Details",
  mounted() {
    this.$store.dispatch("getCarById", this.$route.params.id)
  },
  data() {
    return {}
  },
  computed: {
    car() {
      return this.$store.state.activeCar
    }
  },
  methods: {
    deleteCar() {
      this.$store.dispatch("deleteCar", this.car._id)
    },
    bid() {
      let bid = { id: this.car._id, price: this.car.price + 100 }
      this.$store.dispatch("bid", bid)
    }
  }
}
</script>

<style>
</style>