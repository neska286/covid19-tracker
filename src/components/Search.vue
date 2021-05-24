<template>
    <div class="search">
        <div class="container">
             <div class="card" style="width: 50rem;">
   <form class="pt-5">
  <div class="form-row ">
    <div class="col-sm-8 my-1 ml-5 input-container">
        <i class="fas fa-search icon"></i>
      <input type="text" class="form-control input-field"  v-model="country" >
    </div>
    <div class="col-auto my-1">
      <button type="submit" @click.prevent="getData" class="btn btn-main">Search</button>
    </div>
  </div>
</form>

      <div class="row pt-5" >
     <div class="col-md-4">
         <p>Cases: {{ cases}}</p>
     </div>
     <div class="col-md-4">
         <p>Death: {{death}}</p>
     </div>
     <div class="col-md-4">
         <p>Recoverd: {{ recovered}}</p>
     </div>
 </div>

     </div>

</div>

    </div>

    
    
</template>

<script>
    export default {
        name:'Search',
        data() {
            return {
                country:'',
                countryList: [],
                cases:'',
                death:'',
                recovered:''
            }
        },
          methods: {
            getCovidData() {
                fetch('https://covid-193.p.rapidapi.com/countries',{
                    "method":"GET",
                    "headers":{
                    "x-rapidapi-host": "covid-193.p.reapidapi.com",
                    "x-rapidapi-key":"f117361379msh12d7883431ee443p12c955jsn407e7c123c7a"
                    }
                }).then(response=> response.json()).then((data)=>{
                    console.log(data.response)
                    this.countryList = data.response 
                }).catch((error)=>{
                    console.log(error)
                })
            },
            getData(){
                              fetch('https://covid-193.p.rapidapi.com/statistics?country='+ this.country,{
                    "method":"GET",
                    "headers":{
                    "x-rapidapi-host": "covid-193.p.reapidapi.com",
                    "x-rapidapi-key":"f117361379msh12d7883431ee443p12c955jsn407e7c123c7a"
                    }
                }).then(response=> response.json()).then((data)=>{
                    data = data.response[0];
                    this.cases = data.cases.total;
                     this.death = data.deaths.total;
                      this.recovered = data.cases.recovered;
                }).catch((error)=>{
                    console.log(error)
                })

            }
        },
        created(){
         
        }
        
    }
</script>

<style lang="scss" scoped>
.btn-main{
    background-color: #3B7F91;
    color: white;
}

   .input-icons i {
            position: absolute;
        }
          
        .input-icons {
            width: 100%;
            margin-bottom: 10px;
        }
          
        .input-field {
            width: 100%;
            padding: 10px;
            text-align: left;
        }
      /* Style the input container */
.input-container {
  display: flex;
  width: 100%;
  margin-bottom: 15px;
}
.icon {
  padding: 10px;
  background: rgb(161, 161, 161);
  color: white;
  min-width: 50px;
  text-align: left;
}
        

</style>