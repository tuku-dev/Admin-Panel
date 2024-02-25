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
    <span
      class="sidebar-toggler bg-cyan-950 hover:bg-cyan-900 flex items-center justify-center"
      @click="toggleSidebar"
    >
      <IconsRightCaret />
    </span>
  </div>
</template>
