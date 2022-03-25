<script>
   import Controller from "./components/Controller.svelte";
	import Result from "./components/Result.svelte";

   let info = {
      text: "",
      size: 0,
      width: 0,
      letterSpacing: 0,
      color: "",
      worldSpacing: 0,
      textTransform: ""
   }
   
   function passText(e) {
      
      info.text = e.detail.text;
      info.size = e.detail.s;
      info.width = e.detail.w;
      info.letterSpacing = e.detail.l;
      info.color = e.detail.c;
      info.worldSpacing = e.detail.ws;
      info.textTransform = e.detail.tt;

   }
</script>


<style>


    .title {
       color: blue;
       text-align: center;
       font-size: 2em;
       margin-top: 10px;
    }
    .sub-title {
      color: #A9A9A9;
       text-align: center;
       font-size: .9em;
       letter-spacing: .2em;
       margin-bottom: 40px;
    }
    .copyright {
       margin: 40px 0 20px 20px;
       color: #A9A9A9;
       font-size: .9em;
    }
    @media only screen and (max-width: 600px) {
       .title {
          font-size: 1.5em;
       }
       .sub-title {
          font-size: .6em;
          letter-spacing: .1em;
       }
    }
</style>


<h1 class="title">Text Editor</h1>
<Controller on:message={passText}/>
<Result {...info}/>
<p class="copyright"><span>&copy;</span> 2022 EL malhouni Rayyane</p>