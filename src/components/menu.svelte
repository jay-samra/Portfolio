  <!-- Hamburger menu is clickable and closes, need to add the onclick menu screen -->
  <script>
    let isActive = false;
  
    function toggleMenu() {
      isActive = !isActive;
    }
  </script>
  
  <button
  type="button"
  class="tham tham-e-squeeze tham-w-8 {isActive ? 'tham-active' : ''}"
  on:click={toggleMenu}
  aria-expanded={isActive}
  aria-label="Toggle menu"
>
  <div class="tham-box">
      <div class="tham-inner"></div>
  </div>
</button>


  
  <style>
  
    div {
      margin: 1rem;
    }
  </style>