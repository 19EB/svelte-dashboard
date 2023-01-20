<script lang="ts">
    
    import { preferences } from '../util/store';
    $: currentTheme = $preferences.theme;

    afterUpdate(() => {
        if (currentTheme === 'dark') {
            document.documentElement.classList.add('dark')
        } else {
            document.documentElement.classList.remove('dark')
        }
    });

	import '../app.postcss';
	import Drawer from '../components/Drawer.svelte';
    import Navbar from '../components/Navbar.svelte';
	import { afterUpdate } from 'svelte';

    let drawerOpen = true;

</script>

<Navbar toggleDrawer={()=>drawerOpen=!drawerOpen} />
<div class="flex flex-row flex-shrink-1 dark:bg-gray-800">
    <Drawer expanded={drawerOpen} />
    <div id="main-content" class="flex-shrink-1 w-full h-full p-10 overflow-x-hidden mt-14">
        <slot/>
    </div>
</div>
