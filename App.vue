<template>
<div>
  <h1 id="hh">{{header}}</h1>
  
<input id="ii" v-model="newitem" placeholder="enter task to add in list" v-on:keyup.enter="additem">

    <button id="ad" @click="additem">add item</button>
 
 <button id="rese" type="reset" @click="change">reset</button>

 <button id="del" @click="deleteitem">delete item</button>

 <ol id="oo">
    
    <li  style="text-decoration:underline;" v-for="item in items" v-bind:key="item.id">{{item}}</li></ol>
  </div>
</template>

<script>

export default {
  name:'#idd',
  data(){
    return {
      header:"SHOPPING-LIST",
      items:[],
      newitem:''
    }
  },
 
  methods:{
     additem(){
       if(this.newitem===''){alert("enter the task");return;}
       return this.items.push(this.newitem)
     
  },
  change(){
    this.items=[]
  },
  deleteitem(){
    return this.items.pop();
  }
}
}


</script>

<style>

html{
   padding-left: 25%;
   background-color: coral;
   background-repeat: no-repeat;
}
#hh{
  font-size: 500%;
  scrollbar-shadow-color: tan;
  color:red
}
#ii{

  width: 50%;
  height: 70px;
  
  font-size: 30px;
 
}
#rese{
   margin-top: 0px;
  background-color:aquamarine;
   margin-top: -200px; 
   margin-left:5px;

  width:100px;

}
#ad{
   margin-top: -5000px;
   background-color: burlywood;
   margin-left:5px;
    
  width:100px;


}
#del{
  background-color:bisque;
   
  margin-left:5px;
  width:100px;
}
#oo{
  width: 360px;
  border: 15px solid yellowgreen;
  padding: 50px;
  margin-left:0px;
  margin-top: 50px;
}
</style>
