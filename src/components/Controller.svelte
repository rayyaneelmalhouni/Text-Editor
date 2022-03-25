<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher()
    const cssColors = [
  "AliceBlue",
  "AntiqueWhite",
  "Aqua",
  "Aquamarine",
  "Azure",
  "Beige",
  "Bisque",
  "Black",
  "BlanchedAlmond",
  "Blue",
  "BlueViolet",
  "Brown",
  "BurlyWood",
  "CadetBlue",
  "Chartreuse",
  "Chocolate",
  "Coral",
  "CornflowerBlue",
  "Cornsilk",
  "Crimson",
  "Cyan",
  "DarkBlue",
  "DarkCyan",
  "DarkGoldenRod",
  "DarkGray",
  "DarkGrey",
  "DarkGreen",
  "DarkKhaki",
  "DarkMagenta",
  "DarkOliveGreen",
  "DarkOrange",
  "DarkOrchid",
  "DarkRed",
  "DarkSalmon",
  "DarkSeaGreen",
  "DarkSlateBlue",
  "DarkSlateGray",
  "DarkSlateGrey",
  "DarkTurquoise",
  "DarkViolet",
  "DeepPink",
  "DeepSkyBlue",
  "DimGray",
  "DimGrey",
  "DodgerBlue",
  "FireBrick",
  "FloralWhite",
  "ForestGreen",
  "Fuchsia",
  "Gainsboro",
  "GhostWhite",
  "Gold",
  "GoldenRod",
  "Gray",
  "Grey",
  "Green",
  "GreenYellow",
  "HoneyDew",
  "HotPink",
  "IndianRed",
  "Indigo",
  "Ivory",
  "Khaki",
  "Lavender",
  "LavenderBlush",
  "LawnGreen",
  "LemonChiffon",
  "LightBlue",
  "LightCoral",
  "LightCyan",
  "LightGoldenRodYellow",
  "LightGray",
  "LightGrey",
  "LightGreen",
  "LightPink",
  "LightSalmon",
  "LightSeaGreen",
  "LightSkyBlue",
  "LightSlateGray",
  "LightSlateGrey",
  "LightSteelBlue",
  "LightYellow",
  "Lime",
  "LimeGreen",
  "Linen",
  "Magenta",
  "Maroon",
  "MediumAquaMarine",
  "MediumBlue",
  "MediumOrchid",
  "MediumPurple",
  "MediumSeaGreen",
  "MediumSlateBlue",
  "MediumSpringGreen",
  "MediumTurquoise",
  "MediumVioletRed",
  "MidnightBlue",
  "MintCream",
  "MistyRose",
  "Moccasin",
  "NavajoWhite",
  "Navy",
  "OldLace",
  "Olive",
  "OliveDrab",
  "Orange",
  "OrangeRed",
  "Orchid",
  "PaleGoldenRod",
  "PaleGreen",
  "PaleTurquoise",
  "PaleVioletRed",
  "PapayaWhip",
  "PeachPuff",
  "Peru",
  "Pink",
  "Plum",
  "PowderBlue",
  "Purple",
  "RebeccaPurple",
  "Red",
  "RosyBrown",
  "RoyalBlue",
  "SaddleBrown",
  "Salmon",
  "SandyBrown",
  "SeaGreen",
  "SeaShell",
  "Sienna",
  "Silver",
  "SkyBlue",
  "SlateBlue",
  "SlateGray",
  "SlateGrey",
  "Snow",
  "SpringGreen",
  "SteelBlue",
  "Tan",
  "Teal",
  "Thistle",
  "Tomato",
  "Turquoise",
  "Violet",
  "Wheat",
  "White",
  "WhiteSmoke",
  "Yellow",
  "YellowGreen",
];
    let texty = "";
    let size = 16;
    let width = 500;
    let letterSpacing = 2;
    let color = "Black";
    let worldSpacing = 8;
    let textTransform = "";
    

    function sendText() {
         dispatch("message", {
             text: texty,
             s: size,
             w: width,
             l: letterSpacing,
             c: color.toLocaleLowerCase(),
             ws: worldSpacing,
             tt: textTransform
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
   .v select {
    margin: 10px 0;
    width: 120px;
    padding: 5px;
    border: none;
    background-color: #F9F9F9;

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
        <div class="space-container" >
            <h3>World spacing: </h3>
        <input  type="range" min=0 max=46 class="space-controll c" bind:value={worldSpacing} on:change={sendText}/>
        </div>
        
    </div>
    <div class="select-case">
        <div class="size-container v" >
            <h3>Color: </h3>
            <select id="cars" name="cars" bind:value={color} on:change={sendText}>
                {#each cssColors as color}
                    <option value={color}>{color.toUpperCase()}</option>
                {/each}
              </select>
            </div>
            <div class="size-container v" >
                <h3>Text transform: </h3>
                <select id="transformText" name="transformText" bind:value={textTransform} on:change={sendText}>
                        <option value="">Normal</option>
                        <option value="capitalize">Capitalise</option>
                        <option value="uppercase">UPPERCASE</option>
                        <option value="lowercase">lowercase</option>
                  </select>
            </div>
        </div>
         
        

</div>
<div class="textarea">
    <h2>Write text here: </h2>
    <textarea name="" id="" cols="30" rows="10" bind:value={texty} on:keyup={sendText}></textarea>
</div>