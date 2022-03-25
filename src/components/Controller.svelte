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
       margin: 20px;
       margin-top: 30px;
       text-align: center;
   }
   .textarea h2 {
       font-size: 1.2em;
       margin-bottom: 15px;
   }
   .textarea textarea{
       width: 100%;
       max-width: 750px;
       max-height: 400px;
       padding: 10px;
       border-radius: 15px;
       background-color: #F9F9F9;
       border: none;
   }

</style>

<div class="controller">
    <div class="range">
        <div class="size-container" >
            <h3>Size: </h3>
        <input  type="range" min=0 max=36 class="size-controll c"/>
        </div>
        <div class="width-container" >
            <h3>Width: </h3>
        <input  type="range" min=0 max=1000 class="width-controll c"/>
        </div>
        <div class="space-container" >
            <h3>letter-spacing: </h3>
        <input  type="range" min=0 max=26 class="space-controll c"/>
        </div>
    </div>
    <div class="select-case">
        <div class="size-container" >
            <h3>Color: </h3>
            <select id="cars" name="cars">
                <option value="volvo">Volvo</option>
                <option value="saab">Saab</option>
                <option value="fiat">Fiat</option>
                <option value="audi">Audi</option>
              </select>
            </div>
        <div class="font-container" >
             <h3>Fonts: </h3>
            <select id="cars" name="cars">
                <option value="volvo">Roboto</option>
                <option value="saab">Poppins</option>
                <option value="fiat">Arial</option>
            </select>
         </div>
        </div>
         
        

</div>
<div class="textarea">
    <h2>Write text here: </h2>
    <textarea name="" id="" cols="30" rows="10"></textarea>
</div>