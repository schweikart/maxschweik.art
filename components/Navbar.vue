<template>
  <div class="flex justify-between max-w-2xl px-4 py-4 mx-auto sm:px-8">
    <!-- Navigation -->
    <div class="text-gray-700 dark:text-gray-200">
      <ContentNavigation v-slot="{ navigation }">
        <NuxtLink
          v-for="link of navigation"
          :key="link._path"
          :to="link._path"
          active-class="font-bold"
          class="mr-4"
        >
          {{ link.navTitle || link.title }}
        </NuxtLink>
      </ContentNavigation>
    </div>
    <!-- Social icons & Color Mode -->
    <div class="space-x-3 text-gray-500 transition">
      <a href="https://www.instagram.com/maxschweikart" title="Instagram" class="hover:text-gray-700 dark:hover:text-gray-300"><Icon name="fa-brands:instagram" /></a>
      <a href="https://github.com/schweikart" title="GitHub" class="hover:text-gray-700 dark:hover:text-gray-300"><Icon name="fa-brands:github" /></a>
      <ColorModeSwitch class="hover:text-gray-700 dark:hover:text-gray-300" />
    </div>
  </div>
</template>
