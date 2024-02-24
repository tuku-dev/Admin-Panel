<script setup>
const sidebarState = useSidebarState();
</script>
<template>
  <div>
    <div class="wrapper" :class="{ squeezed: sidebarState }">
      <!-- <div class="wrapper squeezed"> -->
      <div class="sidebar">
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
