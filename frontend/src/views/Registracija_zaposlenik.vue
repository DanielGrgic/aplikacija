<template>
  <div class="pozadina">
    <div class="login">
      <div class="naslov">
        <h1><strong>Work from <span style="color:rgb(146, 187, 214)">home</span></strong></h1>
        <h2 style="color: rgb(150, 187, 220)"><strong>Sign up</strong></h2>
      </div>
      <form v-if="i==1">
        <div class="form-group">
          <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Email">
        </div>
        <div class="form-group">
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
        </div>
      </form>
      <button v-if="i==1" v-on:click = "prikaz" type="submit" class="btn btn primary" style="width:15%; height:70px; border-radius: 100%;"><i class="fa fa-arrow-right" style="font-size:40px;"></i></button>
      <form v-if="i==2">
        <div class="form-group">
          <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="First name">
        </div>
        <div class="form-group">
          <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Last name">
        </div>
        <div class="form-group">
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="How old are you?">
        </div>
        <div class="form-group">
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Country">
        </div>
        <div class="form-group">
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="City">
        </div>
      </form>
      <button v-if="i==2" v-on:click = "prikaz"  type="submit" class="btn btn primary" style="width:15%; height:70px; border-radius: 100%;"><i class="fa fa-arrow-right" style="font-size:40px;"></i></button>
      <form v-if="i==3">
        <div class="form-group">
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Which skills do you have?">
        </div>
        <div class="form-group">
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Minimum hourly rate">
        </div>
        <div class="form-group">
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Anything else?">
        </div> 
        <router-link to="/Naslovna"><button type="submit" class="btn btn primary">Sign up</button></router-link>
      </form>
    </div>
  </div>    
</template>

<script>

export default {
  data (){
    return{
      i:1,
    }
  },
  methods: {
    prikaz(){
      this.i=this.i+1;
    },
  }
}
</script>

<style scoped>
  .pozadina{
    
    width: 100%;
    min-height: 700px;
    
  }
  .login{
    background-color:white;
    width: 30%;
    margin: 5% auto;
    padding: 2% 0;
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    box-shadow: 9px 9px 7px gray;
  }
  .naslov{
    border-bottom: 1.5px solid 	rgb(233, 230, 230);
    width: 80%;
    margin: auto;
    margin-bottom: 10%;
  }

  form{
    width: 80%;
    margin: auto;
  }
  .form-group{
    margin: 6% 3%;
    clear: both;
  }
  input{
    padding: 6%;
    font-size: 18px;
    background-color:white;
    border: rgb(233, 230, 230) 3px solid;
    
  }
   button{
    font-size: 20px;
    width: 60%;
    margin:auto;
    background-color:rgb(146, 187, 214);
    border: none;
    padding: 3%;
    color: white;
    margin-top: 20px;
    font-weight: bold;
  }
    button:hover{
     box-shadow: 9px 9px 7px gray;
    }

  @media(max-width: 600px){

   .login{
    width: 70%;
    border-radius: 20px;
    margin: 10% auto;
    padding: 2% 0;
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    background-color: #dfd7da;
  }

}

</style>