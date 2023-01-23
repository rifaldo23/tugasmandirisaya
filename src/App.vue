<template>
  <div>helllo {{ datasensor }} {{ datasensor2 }}
  <button @click="getData" class="bg-orange-500 p-2 rounded-xl">Ambil Data</button> &nbsp;
  <button @click="getData" class="bg-orange-500 p-2 rounded-xl">Ambil Data satunya</button>
  </div>
</template>

<script> //tempat ngoding java script
export default {
  data(){
    return{
      datasensor : "90",
      datasensor2 : "80"
    }
  },
  created(){
    //this.getData()
   // this.getData1()
  },
  methods: {
    //getData1(){
    //  alert('hello')
   // },
    async getData(){
      const data = await fetch("http://localhost/sensor1")
      const datajson = await data.json()
      console.log(datajson)
      this.datasensor = datajson.sensor1
    
      
      }

  },

}
</script>

<style>

</style>