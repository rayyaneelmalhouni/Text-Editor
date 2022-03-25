<script>
   import Controller from "./components/Controller.svelte";
	import Result from "./components/Result.svelte";
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
<h2 class="sub-title">By Rayyane El-malhouni</h2>
<Controller />
<Result />