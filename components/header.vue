<template>
  <div class="header-inner flex ml-auto h-full max-w-fit">
    <div class="notification"></div>
    <div
      class="user-controls px-4 py-3 flex gap-2 items-center cursor-pointer"
      @click="toggleSubmenu()"
    >
      <span>Hi, John</span>
      <IconsUser />
    </div>
    <ul class="user-links absolute" :class="{ open: userDropdown }">
      <li class="link-item">
        <NuxtLink to="/" class="px-3 p-2 block link">Update Profile</NuxtLink>
      </li>
      <li class="link-item">
        <NuxtLink to="/" class="px-3 p-2 block link">Forgot Password</NuxtLink>
      </li>
      <li class="link-item">
        <NuxtLink to="/" class="px-3 p-2 block link">Change Password</NuxtLink>
      </li>
      <li class="link-item">
        <NuxtLink to="/" class="px-3 p-2 block link">Log Out</NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userDropdown: false,
    };
  },
  methods: {
    toggleSubmenu() {
      this.userDropdown = this.userDropdown ? false : true;
    },
  },
};
</script>
