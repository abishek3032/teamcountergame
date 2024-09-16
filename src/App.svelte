<script>
  let red = 0
  let green = 0
  let blue = 0
</script>
<div>
  <h1>color picker</h1>
  <h1>Red {red}</h1>
  <input type="range" max="255" min="0" bind:value={red}>
  <h1>Green {green}</h1>
  <input type="range" max="255" min="0" bind:value={green}>
  <h1>Blue {blue}</h1>
  <input type="range" max="255" min="0" bind:value={blue}>
  <div style="background: rgb({red}, {green}, {blue}); height:300px; width:300px">
  </div>
  <p>rgb({red}, {green}, {blue})</p>
</div>
