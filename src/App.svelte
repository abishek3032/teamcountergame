<script>
  let redScore = 20
  let blueScore = 20
  const reset= () => {
    redScore = 20
    blueScore = 20
  }
</script>
<div class="px-[5%]">
  <div>
    <div class="mt-5">
      <p class="text-4xl">Team Red <span class="text-red-500">{redScore}</span></p>
      <button on:click={()=>redScore++} class="bg-black px-4 py-2 text-white outline-none">+</button>
      <button on:click={()=>redScore--} class="bg-black px-4 py-2 text-white outline-none">-</button>
    </div>
    <div>
      <p class="text-4xl">Team Blue <span class="text-blue-500">{blueScore}</span></p>
      <button on:click={()=>blueScore++} class="bg-black px-4 py-2 text-white outline-none">+</button>
      <button on:click={()=>blueScore--} class="bg-black px-4 py-2 text-white outline-none">-</button>
  
      {#if redScore <= 0}
        <p class="text-4xl text-blue-500">Blue Team Wins</p>
        <button on:click={reset} class="block bg-yellow-300 text-black px-5 py-2 mt-2 outline-none">New Game</button>
      {/if}
      {#if blueScore <= 0}
        <p class="text-4xl text-red-500">Red Team Wins</p>
        <button on:click={reset} class="block bg-yellow-300 text-black px-5 py-2 mt-2 outline-none">New Game</button>
      {/if}
      {#if redScore >0  && blueScore > 0}
        <button on:click={reset} class="block bg-yellow-300 text-black px-5 py-2 mt-2 outline-none">Reset Game</button>
      {/if}
    </div>
  </div>
</div>