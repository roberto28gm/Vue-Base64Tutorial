<script>
export default {
  methods: {
    decodeBase64() {
      console.log("Text Value: " + this.textvalue);
      let dataDecoded = btoa(this.textvalue);
      alert(dataDecoded);
      this.textDecoded = dataDecoded;
    }
  }
}

</script>

<template>
  <form @submit.prevent="decodeBase64">
    <div class="row">
      <div class="col">
        <input v-model="textvalue" type="text" class="form-control" placeholder="Enter Base 64 value">
      </div>
      <div class="col">
        <button type="submit" class="btn btn-primary mb-2">Decode</button>
      </div>
    </div>
    
    <div class="form-group">
      <p>Decoded value:  {{ textDecoded }}  </p>
    </div>    

  </form>
</template>

<style scoped>
p{
  background-color: #eee;
  margin-top: 1rem;
  padding: 1rem;
  border-radius: 0.5rem;
}
</style>