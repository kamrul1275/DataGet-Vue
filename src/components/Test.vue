<template>
     <div class="hello">
       <h1>Post part.......</h1>
       
<div v-for="post in posts" :key="post.id">

     <h2>{{ post.title}}</h2>
<p>{{ post.body}}</p>

</div>

     
     </div>
   </template>
   
   <script>


import axios from 'axios';

   export default {
     name: 'TestVue',

     data(){

return{

posts:[],

}

},methods:{

},


created(){

axios.get('https://jsonplaceholder.typicode.com/posts')
.then(response=>{

this.posts=response.data



})
.catch(error=>{
     console.log(error);  
});
    
}

     }
    
   
   </script>
   
 