<script>
  import TitleSection from "./sections/TitleSection.svelte";
  import FirstStat from "./sections/FirstStat.svelte";
  import { fade } from 'svelte/transition';

  let showFirstStat = false;

  // Listen for scroll and toggle sections
  function handleScroll() {
    showFirstStat = window.scrollY > window.innerHeight / 1;
  }

  // Set up scroll listener on mount
  import { onMount, onDestroy } from 'svelte';
  onMount(() => {
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });

</script>

<main>
      <TitleSection />
      <div style="height: 100vh;"></div> <!-- Spacer for scroll testing -->
   
  {#if showFirstStat}
    <div transition:fade>
      <FirstStat />
    </div>
  {/if}
</main>

<style>
 
</style>