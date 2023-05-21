<script lang="ts">
  import SVG from "@elements/SVG.svelte"
  import sun from '/icons/sun.svg';
  import moon from '/icons/moon.svg';

  let theme = { sun: true };
  
  function toggle() {
      theme.sun = !theme.sun;
  }


</script>

{#if theme.sun}
<button on:click={toggle} >
    <SVG name={'sun'} />
    <img src={sun} alt="sun" />
</button>
{:else}
<button on:click={toggle}>
    
    <SVG name={'moon'} />
    <img src={moon} alt="moon" />
</button> 
{/if}
