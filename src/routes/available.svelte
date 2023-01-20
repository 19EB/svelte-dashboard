<script>
    import { Indicator, Avatar, Badge } from 'flowbite-svelte'
  </script>
  
  <ul class="divide-y divide-gray-200 dark:divide-gray-700 w-full">
      <li class="py-3 sm:py-4">
          <div class="flex items-center space-x-3">
                  <Avatar />
              <div class="flex-1 min-w-0">
                  <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">User 1</p>
                  <p class="text-sm text-gray-500 truncate dark:text-gray-400">user1@seb.gg</p>
              </div>
              <Badge color="green" rounded class="px-2.5 py-0.5">
                  <Indicator color="green" size="xs" class="mr-1"/>Available
              </Badge>
          </div>
      </li>
      <li class="py-3 sm:py-4">
        <div class="flex items-center space-x-3">
                <Avatar />
            <div class="flex-1 min-w-0">
                <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">User 2</p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">user2@seb.gg</p>
            </div>
            <Badge color="green" rounded class="px-2.5 py-0.5">
                <Indicator color="green" size="xs" class="mr-1"/>Available
            </Badge>
        </div>
    </li>
    <li class="py-3 sm:py-4">
        <div class="flex items-center space-x-3">
                <Avatar />
            <div class="flex-1 min-w-0">
                <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">User 3</p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">user3@seb.gg</p>
            </div>
            <Badge color="green" rounded class="px-2.5 py-0.5">
                <Indicator color="green" size="xs" class="mr-1"/>Available
            </Badge>
        </div>
    </li>
      <li class="py-3 sm:py-4">
          <div class="flex items-center space-x-3">
              <div class="flex-shrink-0">
                  <Avatar />
              </div>
              <div class="flex-1 min-w-0">
                <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">User 4</p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">user4@seb.gg</p>
              </div>
              <Badge color="red"  rounded class="px-2.5 py-0.5">
                  <Indicator color="red" size="xs" class="mr-1"/>Unavailable
              </Badge>
          </div>
      </li>
      <li class="py-3 sm:py-4">
        <div class="flex items-center space-x-3">
            <div class="flex-shrink-0">
                <Avatar />
            </div>
            <div class="flex-1 min-w-0">
              <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">User 5</p>
              <p class="text-sm text-gray-500 truncate dark:text-gray-400">user5@seb.gg</p>
            </div>
            <Badge color="red"  rounded class="px-2.5 py-0.5">
                <Indicator color="red" size="xs" class="mr-1"/>Unavailable
            </Badge>
        </div>
    </li>
    <li class="py-3 sm:py-4">
        <div class="flex items-center space-x-3">
            <div class="flex-shrink-0">
                <Avatar />
            </div>
            <div class="flex-1 min-w-0">
              <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">User 6</p>
              <p class="text-sm text-gray-500 truncate dark:text-gray-400">user6@seb.gg</p>
            </div>
            <Badge color="red"  rounded class="px-2.5 py-0.5">
                <Indicator color="red" size="xs" class="mr-1"/>Unavailable
            </Badge>
        </div>
    </li>
    <li class="py-3 sm:py-4">
        <div class="flex items-center space-x-3">
            <div class="flex-shrink-0">
                <Avatar />
            </div>
            <div class="flex-1 min-w-0">
              <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">User 7</p>
              <p class="text-sm text-gray-500 truncate dark:text-gray-400">user7@seb.gg</p>
            </div>
            <Badge color="red"  rounded class="px-2.5 py-0.5">
                <Indicator color="red" size="xs" class="mr-1"/>Unavailable
            </Badge>
        </div>
    </li>
  </ul>