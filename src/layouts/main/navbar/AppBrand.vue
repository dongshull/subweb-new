<template>
  <div class="navbar-brand app-brand demo d-flex py-0 py-lg-2 me-4">
    <!-- Mobile menu toggle: Start-->
    <button
      class="navbar-toggler border-0 px-0 me-2"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
      @click="$store.commit('MAIN_LAYOUT_MENU_EXPAND')"
    >
      <i class="ti ti-menu-2 ti-sm align-middle"></i>
    </button>
    <!-- Mobile menu toggle: End-->
    <router-link to="/" class="app-brand-link">
      <span class="app-brand-logo demo">
        <img src="/favicon.png" alt="Logo" class="app-logo" style="height: 32px; width: auto;" />
      </span>
      <span class="app-brand-text demo menu-text fw-bold ms-2 ps-1">{{ siteName }}</span>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'AppBrand',
  data() {
    return {
      siteName: '',
    };
  },
  created() {
    this.siteName = window.config.siteName;
  },
};
</script>

<style scoped>
.app-logo {
  height: 32px; /* 根据需要调整 logo 的高度 */
  width: auto; /* 自动调整宽度，保持比例 */
}
</style>
