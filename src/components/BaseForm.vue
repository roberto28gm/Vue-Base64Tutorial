<script>
export default {
  props: {
    todo: Object
  },
  methods: {
    decodeBase64: function (event) {
      alert("test");
    }
  }
}
</script>

<template>
  <form @submit.prevent="decodeBase64">
    <div class="row">
      <div class="col">
        <input v-model="textValue" type="text" class="form-control" placeholder="Enter Base 64 value">
      </div>
      <div class="col">
        <button type="submit" class="btn btn-primary mb-2">Decode</button>
      </div>
    </div>
    
    <div class="form-group">
      <label for="decodedValue">Decoded value</label>
      <textarea v-model="textArea" class="form-control" id="decodedValue" rows="3"></textarea>
    </div>    

  </form>
</template>
