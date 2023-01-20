<script lang="ts">
    import { Heading, P } from 'flowbite-svelte';
    import { Skeleton } from 'flowbite-svelte'
	import Accordions from './accordions.svelte';
	import Activity from './activity.svelte';
	import Available from './available.svelte';
	import Timeline from './timeline.svelte';
</script>

<div class="w-full">
    
    <div class="w-full grid grid-cols-1 lg:grid-cols-2 2xl:grid-cols-4 gap-5">

        <div class="w-full p-5 bg-indigo-700">
            <Heading tag="h4">top-card-1</Heading>
            <Skeleton class="mt-5"/>
        </div>

        <div class="w-full p-5 bg-red-400">
            <Heading tag="h4">top-card-2</Heading>
            <Skeleton class="mt-5"/>
        </div>

        <div class="w-full p-5 bg-green-300">
            <Heading tag="h4">top-card-3</Heading>
            <Skeleton class="mt-5"/>
        </div>

        <div class="w-full p-5 bg-orange-500">
            <Heading tag="h4">top-card-4</Heading>
            <Skeleton class="mt-5"/>
        </div>

    </div>

    <div class="w-full grid grid-cols-1 lg:grid-cols-2 gap-5 mt-5">

        <div class="border-2 dark:border-gray-700 rounded-md w-full p-5">
            <Heading tag="h4">Timeline</Heading>
            <hr class="mb-5"/>
            <Timeline />
        </div>

        <div class="border-2 dark:border-gray-700 rounded-md w-full p-5">
            <Heading tag="h4">Activity</Heading>
            <hr class="mb-5"/>
            <Activity />
        </div>
    </div>

    <div class="w-full grid grid-cols-1 xl:grid-cols-3 gap-5 mt-5">
        <div class="border-2 dark:border-gray-700 rounded-md w-full p-5">
            <Heading tag="h4">Accordions</Heading>
            <hr class="mb-5"/>
            <Accordions />
        </div>

        <div class="border-2 dark:border-gray-700 rounded-md w-full p-5">
            <Heading tag="h4">Staff</Heading>
            <hr class="mb-5" />
            <Available />
        </div>

        <div class="border-2 dark:border-gray-700 rounded-md w-full p-5">
            <Heading tag="h4">Box 3</Heading>
            <hr/>
            <P class="mt-5">
                Dui ut ornare lectus sit amet est placerat. Non sodales neque sodales ut etiam. Lectus proin nibh nisl condimentum id venenatis a condimentum vitae. Magna ac placerat vestibulum lectus mauris. Urna molestie at elementum eu. Elit ullamcorper dignissim cras tincidunt. Elit pellentesque habitant morbi tristique senectus et netus et malesuada. Pulvinar sapien et ligula ullamcorper. Tincidunt ornare massa eget egestas purus. Vitae justo eget magna fermentum. Vehicula ipsum a arcu cursus vitae congue. Volutpat maecenas volutpat blandit aliquam. Dis parturient montes nascetur ridiculus mus. Urna neque viverra justo nec ultrices dui sapien eget. Facilisis gravida neque convallis a cras semper. Amet nisl suscipit adipiscing bibendum est ultricies. Molestie at elementum eu facilisis sed odio.
            </P>
        </div>
    </div>

</div>