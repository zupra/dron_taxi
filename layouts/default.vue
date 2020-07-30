<template lang="pug">
.Grid
  .Header
    N-link.logo(
      to="/"
    ) DRON TAXI
  .Sidebar.flex_col.x_sb
    .Nav
      N-link.Nav_item(
        v-for="link,idx in NAV"
        :to="`/${link.val}`"
        :class="`i_${idx+1}`"
      ) {{link.name}}
    
    .Nav_item.i_4 Выход
  .Main
    <Nuxt />

</template>

<script>
const DATA = [
  { name: 'Профиль', val: 'profile' },
  { name: 'Упр. пользователями', val: 'config-users' },
  { name: 'Упр. ролями', val: 'config-roles' },
]

export default {
  layout: 'blank',
  data() {
    return {
      NAV: DATA,
    }
  },
}
</script>

<style>
/*
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*/
</style>
