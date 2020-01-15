<template>
  <div class="app-nav">
    <div class="container topbar">
      <vs-row vs-w="12">
        <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-lg="2" vs-sm="6" vs-xs="6">
          <vs-icon icon="email"></vs-icon>
          <span class="item-text">contact@q-matters.com</span>
        </vs-col>
        <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-lg="2" vs-sm="6" vs-xs="6">
          <vs-icon icon="phone"></vs-icon>
          <span class="item-text">+52 (81) 1609 6055</span>
        </vs-col>
      </vs-row>
    </div>
    <div class="container">
      <vs-row vs-w="12">
        <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="12">
          <vs-navbar v-model="activeItem" class="navbarx">
            <div slot="title">
              <vs-navbar-title>
                <img src="../assets/logo.png" alt="Quality Matters Logo" class="brand-logo" />
              </vs-navbar-title>
            </div>
            <vs-navbar-item index="0">
              <a href="#">Home</a>
            </vs-navbar-item>
            <vs-navbar-item index="1">
              <a href="#">About</a>
            </vs-navbar-item>
            <vs-navbar-item index="2">
              <a href="#servicesSection">Services</a>
            </vs-navbar-item>
            <vs-navbar-item index="3">
              <a href="#contactSection">Contact</a>
            </vs-navbar-item>
          </vs-navbar>
        </vs-col>
      </vs-row>
    </div>
  </div>
</template>
<script>
export default {
  title: 'AppNav',
  data: () => ({
    activeItem: 0
  })
}
</script>
<style scoped>
@media (max-width: 500px) {
  .topbar > .vs-row > .vs-col {
    font-size: 14px !important;
    overflow-x: hidden;
  }
}
</style>
<style lang="scss">
.container {
  display: block;
}
.container > .vs-row {
  max-width: 1200px;
  margin: 0 auto;
}
.vs-navbar--item > a {
  color: #0f609f !important;
  font-size: 16px !important;
  font-weight: 600;
}
.is-active-item > a {
  color: #3cb065 !important;
  font-weight: 600;
  font-size: 16px !important;
}
.is-active-item::after {
  content: "";
  color: #3cb065;
  background-color: #3cb065;
}
.brand-logo {
  max-height: 52px;
  width: auto;
}
.topbar {
  color: white;
  background: #28395d;
  padding: 0.5rem 1rem !important;
}
.item-text {
  margin-left: 0.5rem;
  font-size: 0.85rem;
}
</style>
