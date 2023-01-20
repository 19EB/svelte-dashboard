<script lang="ts">
	import Sidebar from "./Sidebar.svelte";

    export let expanded = true;

</script>

<div class="mr-0 {expanded ? 'md:mr-80' : 'md:mr-0'} transition-all duration-200"></div>

<div class="{expanded ? 'w-80' : 'w-0'} flex flex-shrink-0 items-start justify-center fixed md:fixed pt-16 mt-1 bg-white dark:bg-gray-900 h-screen z-20 overflow-y-auto transition-all duration-200">
    <Sidebar />
</div>