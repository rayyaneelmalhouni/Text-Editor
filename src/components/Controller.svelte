<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher()
    let texty = "";
    let size = 16;
    let width = 500;
    let letterSpacing = 2;
    let color = "red";
    let font = "arial";
    function sendText() {
         dispatch("message", {
             text: texty,
             s: size,
             w: width,
             l: letterSpacing,
             c: color,
             f: font
        })
    }
</script>

<style>
   .range, .select-case {
       display: flex;
       width: 100%;
       justify-content: space-around;
       flex-wrap: wrap;
       margin-top: 50px;
   }
   .select-case {
       margin-top: 20px;
       margin-bottom: 20px;
   }
   .c {
       margin: 5px;
       margin-bottom: 25px;
   }
   h3 {
       font-size: 1em;
   }
   .textarea {
       margin-top: 30px;
       text-align: center;
   }
   .textarea h2 {
       font-size: 1.2em;
       margin-bottom: 15px;
   }
   .textarea textarea{
       width: 80%;
       max-width: 750px;
       max-height: 400px;
       padding: 10px;
       border-radius: 15px;
       background-color: #F9F9F9;
       border: none;
   }
   @media only screen and (max-width: 600px) {
       .range, .select-case {
           display: block;
           width: 300px;
           margin: 0 auto;
           text-align: center
       }
       .select-case .v {
           margin-bottom: 20px;
       }

   }

</style>

<div class="controller">
    <div class="range">
        <div class="size-container" >
            <h3>Size: </h3>
        <input  type="range" min=0 max=36 class="size-controll c" bind:value={size} on:change={sendText}/>
        </div>
        <div class="width-container" >
            <h3>Width: </h3>
        <input  type="range" min=0 max=1000 class="width-controll c" bind:value={width} on:change={sendText}/>
        </div>
        <div class="space-container" >
            <h3>letter-spacing: </h3>
        <input  type="range" min=0 max=26 class="space-controll c" bind:value={letterSpacing} on:change={sendText}/>
        </div>
    </div>
    <div class="select-case">
        <div class="size-container v" >
            <h3>Color: </h3>
            <select id="cars" name="cars" bind:value={color} on:change={sendText}>
                <option value="red">Red</option>
                <option value="blue">Blue</option>
                <option value="green">Green</option>
                <option value="yellow">Yellow</option>
              </select>
            </div>
        <div class="font-container v" >
             <h3>Font: </h3>
            <select id="cars" name="cars" bind:value={font} on:change={sendText}>
                <option value="roboto">Roboto</option>
                <option value="poppins">Poppins</option>
                <option value="arial">Arial</option>
            </select>
         </div>
        </div>
         
        

</div>
<div class="textarea">
    <h2>Write text here: </h2>
    <textarea name="" id="" cols="30" rows="10" bind:value={texty} on:keyup={sendText}></textarea>
</div>