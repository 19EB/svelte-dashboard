<script lang="ts">
    import { get } from 'svelte/store'
    import { preferences } from '../util/store';

    $: currentTheme = $preferences.theme;

    import { Input, Button, Tooltip } from 'flowbite-svelte'

    export let toggleDrawer:((e: MouseEvent) => void);

    const toggleTheme = () => {
      if(get(preferences).theme === 'dark') {
        preferences.set({theme: 'light'});
      }else {
        preferences.set({theme: 'dark'});
      }
    }

</script>
  

<nav class="z-30 text-black bg-gray-50 dark:bg-gray-900 dark:text-gray-200 border-gray-700 px-2 py-0.5 fixed w-full mx-auto z-20 top-0 left-0 border-b">
  
  <div class="p-2 flex flex-row justify-between">

  <Button color="alternative" class="ml-1" on:click={toggleDrawer}>
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="h-6 w-6 shrink-0" aria-label="bars 3" fill="none" viewBox="0 0 24 24" stroke-width="2"><path d="M3.75 6.75H20.25M3.75 12H20.25M3.75 17.25H20.25" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path> </svg>
  </Button>

  <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
    Svelte Dashboard
  </span>

  <div class="flex md:order-2 gap-2 items-center">
    <Button id="theme-button" color="alternative" on:click={toggleTheme}>
      {#if currentTheme === 'dark'}
      <svg viewBox="0 0 24 24" fill="yellow" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6"><path d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" class="stroke-slate-400 dark:stroke-slate-500"></path><path d="M12 4v1M17.66 6.344l-.828.828M20.005 12.004h-1M17.66 17.664l-.828-.828M12 20.01V19M6.34 17.664l.835-.836M3.995 12.004h1.01M6 6l.835.836" class="stroke-slate-400 dark:stroke-slate-500"></path></svg>
      {:else}
      <svg viewBox="0 0 24 24" fill="none" class="w-6 h-6"><path fill-rule="evenodd" clip-rule="evenodd" d="M17.715 15.15A6.5 6.5 0 0 1 9 6.035C6.106 6.922 4 9.645 4 12.867c0 3.94 3.153 7.136 7.042 7.136 3.101 0 5.734-2.032 6.673-4.853Z" class="fill-transparent"></path><path d="m17.715 15.15.95.316a1 1 0 0 0-1.445-1.185l.495.869ZM9 6.035l.846.534a1 1 0 0 0-1.14-1.49L9 6.035Zm8.221 8.246a5.47 5.47 0 0 1-2.72.718v2a7.47 7.47 0 0 0 3.71-.98l-.99-1.738Zm-2.72.718A5.5 5.5 0 0 1 9 9.5H7a7.5 7.5 0 0 0 7.5 7.5v-2ZM9 9.5c0-1.079.31-2.082.845-2.93L8.153 5.5A7.47 7.47 0 0 0 7 9.5h2Zm-4 3.368C5 10.089 6.815 7.75 9.292 6.99L8.706 5.08C5.397 6.094 3 9.201 3 12.867h2Zm6.042 6.136C7.718 19.003 5 16.268 5 12.867H3c0 4.48 3.588 8.136 8.042 8.136v-2Zm5.725-4.17c-.81 2.433-3.074 4.17-5.725 4.17v2c3.552 0 6.553-2.327 7.622-5.537l-1.897-.632Z" class="fill-slate-400 dark:fill-slate-500"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M17 3a1 1 0 0 1 1 1 2 2 0 0 0 2 2 1 1 0 1 1 0 2 2 2 0 0 0-2 2 1 1 0 1 1-2 0 2 2 0 0 0-2-2 1 1 0 1 1 0-2 2 2 0 0 0 2-2 1 1 0 0 1 1-1Z" class="fill-slate-400 dark:fill-slate-500"></path></svg>
      {/if}
    </Button>
    <Tooltip placement="bottom" triggeredBy="#theme-button">{currentTheme === 'dark' ? 'Switch to light' : 'Switch to dark'}</Tooltip>

    <div class="hidden relative md:block">
      <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 dark:text-white"><path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" /></svg>
      </div>
      <Input id="search-navbar" class="pl-10" placeholder="Search..." />
    </div>
  </div>
</div>
</nav>

  <hr/>