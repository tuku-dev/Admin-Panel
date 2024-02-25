<template>
  <ul class="navigation">
    <li class="nav-item">
      <NuxtLink to="/" title="Dashboard">
        <IconsDashboard /> <span class="link-text">Dashboard</span>
      </NuxtLink>
    </li>
    <li class="nav-item has-sub">
      <span
        class="menu-text"
        title="Categories"
        @click="toggleSubmenu('categories')"
      >
        <IconsCategories />
        <span class="link-text">Categories</span>
        <span class="carat-down">
          <IconsRightCaret />
        </span>
      </span>
      <ul class="submenu" v-if="isSubmenuOpen('categories')">
        <li class="nav-item">
          <NuxtLink to="/categories/add" title="Add Categories">
            <IconsPlus /> <span class="link-text">Add Category</span>
          </NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink to="/categories/view" title="ViewCategories">
            <IconsList /> <span class="link-text">View categories</span>
          </NuxtLink>
        </li>
      </ul>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      openSubmenus: [],
    };
  },
  methods: {
    toggleSubmenu(menu) {
      if (this.isSubmenuOpen(menu)) {
        // Close the submenu if it's open
        this.openSubmenus = this.openSubmenus.filter((item) => item !== menu);
      } else {
        // Open the submenu if it's closed
        this.openSubmenus.push(menu);
      }
    },
    isSubmenuOpen(menu) {
      // Check if the submenu is open
      return this.openSubmenus.includes(menu);
    },
  },
};
</script>
