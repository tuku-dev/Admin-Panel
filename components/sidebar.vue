<script setup>
const sidebarState = useSidebarState();
function toggleSidebar() {
  sidebarState.value = sidebarState.value ? false : true;
}
</script>

<template>
  <div class="sidebar-inner">
    <Logo />
    <hr class="border" />
    <SidebarLinks />
    <span class="sidebar-toggler" @click="toggleSidebar">
      <IconsRightCaret />
    </span>
  </div>
</template>
