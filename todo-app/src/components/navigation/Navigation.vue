<template>
  <div class="navigation">
    <nav class="nav nav-main">
      <ul class="nav__list">
        <li class="nav__item" v-for="link in navLinks">
          <router-link :to="link.href" class="nav__link">{{ link.title }}</router-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navigation',
  data () {
    return {
      navLinks: [
        {
          title: 'Main',
          href: '/'
        },
        {
          title: 'Orders',
          href: '/orders'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>