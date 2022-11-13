<template>
  <div>
    <b-navbar class="m-4">
      <template #brand>
        <b-navbar-item tag="router-link" :to="{ path: '/' }">
          <img src="~assets/images/logo.webp" alt="Lightweight UI components for Vue.js based on Bulma">
        </b-navbar-item>
      </template>
      <template #start>
        <b-navbar-item class="logo" href="/home">
          DI-BI
        </b-navbar-item>
        
      </template>

      <template #end>
        <b-navbar-item tag="div">

          <div class="buttons">
            <b-input class="mx-4" placeholder="Search. through Q&As" type="search" icon="magnify" icon-clickable
              @icon-click="searchIconClick">
            </b-input>
            <b-button size="is-medium" type="is-ghost" icon-right="bell" />
            <b-button size="is-medium" type="is-ghost" icon-right="cog" />
          </div>
        </b-navbar-item>
      </template>
    </b-navbar>

    <section class="main-content columns">
      <aside class="column is-2 section">
        <SideBar />
      </aside>

      <div class="container column is-10">
        <Nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>
<style scoped >
.logo {
  font-weight: 700;
  font-family:monospace;
}
</style>