<script type="ts">
import Toggle from './Toggle.svelte';
import { mode } from './store';
</script>

<main class:dark="{$mode === 'dark'}" class:light="{$mode === 'light'}">
  <h1>My Svelte app template</h1>
  This is my new svelte app. I'm going to try and make nice thinks with it As I have
  learned, you cant put text outside of main.
  <!-- <Toggle /> -->
</main>

<style>
:global(body) {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  margin: 0;
  padding: 0;
}

:root {
  --primary-red: #ff0404;
  --primary-yellow: #fbc352;
  --primary-white: #fff;
  --background-light: #fcf0d8;
  --background-dark: #2b2b2b;
}

h1,
main.light h1 {
  color: #ff0404;
}

main.dark h1 {
  color: var(--primary-yellow);
}

main,
main.light {
  background: var(--background-light);
  color: var(--background-dark);
  padding: 1em;
  height: 100vh;
}

main.dark {
  background: var(--background-dark);
  color: var(--primary-white);
}

@media (prefers-color-scheme: dark) {
  main {
    background: var(--background-dark);
    color: var(--primary-white);
  }
  h1 {
    color: var(--primary-yellow);
  }
}
</style>
