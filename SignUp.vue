<template> 
  <header v-bind:class = "heading"> 
    <h2 v-bind:style = "{fontSize:size + 'px' , 
  fontWeight:weis , fontStyle:sty , textAlign:align ,  
  textTransform:trans}">{{name}}</h2>
  </header> 
  <h2 v-bind:id = "papa">{{mog}}</h2> 
  
  <form v-bind:class = "mama" @submit.prevent = "submitForm"> 
   <input type="text" id = "username" placeholder="username" v-model.trim.lazy = "formValues.username" /> 
   <textarea v-bind:class = "mother"  id="userinfo" placeholder="userinfo" v-model = "formValues.userinfo" cols="30" rows="10"></textarea> 
   <select v-bind:class = "sister"  id="country" v-model = "formValues.country"> 
    <option value="">country</option> 
    <option value="arfghastian">Arfghastian</option> 
    <option value="america">America</option> 
    <option value="canada">Canada</option> 
    <option value="kenya">Kenya</option> 
    <option value="tanzania">Tanzania</option>
   </select> 

   <select v-bind:class = "bro" id="jobLocation" v-model = "formValues.jobLocation"> 
     <option value="">jobLocation</option> 
     <option value="india">India</option> 
     <option value="south america">South America</option> 
     <option value="south africa">South Africa</option> 
     <option value="tanzania">Tanzania</option>
   </select> 
   <label v-bind:class = "bob" for="html">HTML</label> 
   <input v-bind:class = "gog" type="checkbox"  id="html" value = "html" v-model = "formValues.skillSet" /> 
   <label v-bind:class = "koko" for="css">CSS3</label> 
   <input v-bind:class = "pepe" type="checkbox"  id="css" value = "css" v-model = "formValues.skillSet" /> 
   <label v-bind:class = "meme" for="javascript">JavaScript</label> 
   <input v-bind:class = "gosh" type="checkbox"  id="javascript" value = "javascript" v-model = "formValues.skillSet">
   <label v-bind:class = "bok" for="remoteWork">accept terms and conditions</label>
   <input v-bind:class = "baby" type="checkbox"  id="remoteWork" v-model = "formValues.remoteWork" true-value = "yes" false-value = "no" />  
   <button v-bind:class = "dodo" onclick = "alert('you are hacked')" v-on:click = "name = 'burgers'">submit</button>
  </form>
</template> 

<script> 
 export default{ 
    data(){ 
        return{ 
           name:'restaurant', 
           heading:'active', 
           size:18, 
           weis:800, 
           align:'center', 
           sty:'italic', 
           trans:'uppercase', 
           mama:'search-box', 
           paras:'signup', 
           papa:'dad', 
           mother:'mama', 
           sister:'dada', 
           bro:'kaka', 
           dodo:'niggas', 
           bob:'lala', 
           gog:'dod', 
           koko:'coco', 
           pepe:'bell', 
           meme:'mimi', 
           bok:'god', 
           gosh:'gost', 
           baby:'good', 
           formValues:{ 
               username:'', 
               userinfo:'', 
               country:'', 
               jobLocation:'', 
               remoteWork:"no", 
               skillSet:[]
           }
        }
    }, 
    methods:{ 
      submitForm(){ 
        console.log("Form Values" , this.formValues)
      }
    }, 
    computed:{ 
        mog(){ 
          return `${this.paras}`
        }
    }
 }
</script> 

<style lang = "css"> 
  *{ 
    margin:0; 
    padding:0; 
    box-sizing:border-box;
  } 

  .active{ 
      width:100%; 
      padding:10px 15px; 
      background-color:aquamarine; 
      box-shadow:2px 8px 4px rgba(200 , 10 , 0.5);
  } 

  .search-box{ 
      display:flex; 
      align-items:center; 
      justify-content:center; 
      flex-direction:column;
  } 

  input{ 
      outline:none;
  } 

  input[type = "text"]{ 
      width:100%; 
      padding:10px 15px; 
      border:none; 
      border-radius:8px; 
      background:aquamarine; 
      color:#000; 
      font-size:18px;  
      margin-top:30px;
      font-weight:800; 
      font-style:italic; 
      margin-left:5px;
  } 

  input[type = "text"]::placeholder{ 
      color:#000; 
      font-size:18px; 
      font-weight:800; 
      font-style:italic;
  } 

  #dad{ 
     font-size:18px; 
     font-weight:800;  
     text-align:center;
     font-style:italic; 
     text-transform:uppercase; 
     padding-top:20px;
  } 

  .mama{ 
      margin-top:10px; 
      border:1px solid #000; 
      color:#000; 
      font-size:18px; 
      font-weight:800; 
      padding-left:5px;  
      border-radius:8px;
  } 

  .mama::placeholder{ 
      color:#000; 
      font-size:18px; 
      font-weight:800; 
      font-style:italic; 
      text-transform:uppercase; 
      padding-left:10px;
  } 

  .dada{ 
      width:100%; 
      padding:10px 15px; 
      border-radius:8px;  
      margin:10px 0;
      border:none; 
      background:aquamarine; 
      color:#000; 
      font-size:18px; 
      font-weight:800;  
      text-transform:uppercase;
      font-style:italic;
  } 

  .kaka{ 
      width:100%; 
      padding:10px 15px; 
      border-radius:8px;  
      margin:10px 0;
      border:none; 
      background:rgb(213, 169, 26); 
      color:#000;
      font-size:18px; 
      font-weight:800;  
      text-transform:uppercase;
      font-style:italic;
  } 

  .niggas{ 
      width:100%; 
      max-width:200px; 
      padding:10px 15px; 
      border:none; 
      border-radius:1rem; 
      background:rgb(175, 192, 22); 
      color:#000; 
      font-size:18px;  
      font-weight:800; 
      font-style:italic; 
      text-transform:uppercase; 
      margin:10px 0; 
      cursor:pointer; 
      transition:0.3s ease-in-out; 
      box-shadow:2px 8px 4px rgb(141, 15, 103);
  } 

  .niggas:hover{ 
      color:#1a1a1a; 
      background:#fff; 
      border:1px solid #000;
  } 

  .lala{ 
      font-size:18px; 
      font-weight:800; 
      font-style:italic;  
      text-transform:uppercase;
  } 

  .dod{ 
      width:20px; 
      height:20px; 
      margin:auto;  
      margin:10px 0;
      border-radius:8px; 
      border:1px solid #000;
  } 

  .coco{ 
      font-size:18px; 
      font-weight:800; 
      font-style:italic;  
      text-transform:uppercase;
  } 

  .bell{ 
      width:20px;  
      margin:auto;
      height:20px;  
      margin:10px 0;
      border-radius:8px; 
      border:1px solid #000;
  } 

  .mimi{ 
      font-size:18px; 
      font-weight:800; 
      font-style:italic;  
      text-transform:uppercase;
  } 

  .god{ 
      font-size:18px; 
      font-weight:800; 
      font-style:italic;  
      text-transform:uppercase;
  } 

  .gost{ 
      width:20px; 
      height:20px; 
      margin:auto;  
      margin:10px 0;
      border-radius:8px; 
      border:1px solid #000;
  } 

  .good{ 
      width:20px; 
      height:20px;  
      margin:auto;
      margin:10px 0;
      border-radius:8px; 
      border:1px solid #000;
  }
</style>