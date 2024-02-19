<template>
  <div>
    <div class="wrapper">
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
