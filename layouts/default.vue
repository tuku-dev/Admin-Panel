<script setup>
const sidebarState = useSidebarState();
</script>
<template>
  <div>
    <div class="wrapper flex" :class="{ squeezed: sidebarState }">
      <!-- <div class="wrapper squeezed"> -->
      <div class="sidebar text-white">
        <Sidebar />
      </div>
      <div class="content-wrapper">
        <div class="header">
          <Header />
        </div>
        <div class="page-content">
          <slot />
        </div>
      </div>
    </div>
  </div>
</template>
