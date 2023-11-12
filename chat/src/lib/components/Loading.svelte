<!-- I FUCKING HATE ANIMATIONS -->
<style>
  .loader {
  display: flex;
  overflow: hidden;
  width: 100vw;
  height: 100vh;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

.loader-item {
  width: 7px; /* Adjust the width of each loader item as needed */
  height: 7px; /* Adjust the height of each loader item as needed */
  background-color: purple; /* Adjust the background color as needed */
  animation: moveLoader 2s linear infinite;
}


@keyframes moveLoader {
  0% {
    transform: translateX(-100vw);
  }
  100% {
    transform: translateX(100vw);
  }
}
</style>
  
  <div class='loader'>
    {#each Array(5) as _, i}
        <div class='loader-item'></div>
    {/each}
  </div>
