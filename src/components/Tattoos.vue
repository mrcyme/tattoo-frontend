<template>
<div>
  <button @click="myFunction()">Generate</button>
  <br>
  <select v-model="style">
  <option disabled value="">Choisissez</option>
  <option value="minimalistic"><label>Minimalist</label></option>
  <option value="general"><label>General</label></option>
  <option value="tribal"><label>tribal</label></option>
  <option value="watercolor"><label>watercolor</label></option>
  <option value="oneline"><label>One line</label></option>
  </select>
  <br>
  <img v-bind:src=url width="800" height="800">


</div>
</template>
<script>
export default {
  name: 'tattoos',
  props: {
    url : {type: String, default: "https://tattoos.fra1.cdn.digitaloceanspaces.com/general/5/image"+("000" + Math.floor(Math.random() * 1024)).slice(-4)+".jpg"},
    style: {type: String, default: "general" }
  },
  methods:{
    myFunction: function () {
    this.url = "https://tattoos.fra1.cdn.digitaloceanspaces.com/"+this.style+"/"+(Math.floor(Math.random() * 8)+1)+"/image"+("000" + Math.floor(Math.random() * 1024)).slice(-4)+".jpg";
        }
    }

}

</script>
