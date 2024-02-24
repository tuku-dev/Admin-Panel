<script setup>
const sidebarState = useSidebarState();
console.log(sidebarState.value)
function toggleSidebar() {
  sidebarState.value = sidebarState.value ? false : true;
}
</script>

<template>
  <div class="sidebar-inner">
    <Logo />
    <hr class="border" />
    <SidebarLinks />
    <p>sqz: {{ sidebarState }}</p>
    <span class="sidebar-toggler" @click="toggleSidebar">
      <IconsRightCaret />
    </span>
  </div>
</template>
