<script>
import { marked } from "marked"
  export let text;
  export let size;
  export let width;
  export let color;
  export let letterSpacing;
  export let worldSpacing;
  export let textTransform;

</script>

<style>
    

        h1 {
            text-align: center;
            font-size: 1.2em;
            margin-top: 20px;
            margin-bottom: 10px;
        }
        .result-container {
            width: 80%;
            margin: 0 auto;
        }
        @media only screen and (max-width: 600px) {
            .result-container {
                margin: 20px;
            }
            .result {
                font-size: .9em;
            }

        }
</style>


<h1>Result: </h1>
<div class="result-container">
<p class="result" style="color: {color}; font-weight: {width}; letter-spacing: {letterSpacing}px; font-size: {size}px; word-spacing: {worldSpacing}px; text-transform: {textTransform};">{@html marked(text)}</p>



</div>