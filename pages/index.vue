<template lang="pug">
.Index.p-5

  #palette
    each clr in ['#00BFFF','#0087B4', '#7FFF7FD9', '#7FFF7F', '#128312', '#202020', '#D1D9D1', '#747272', '#660066','#800080', '#991199', '#973E95', '#AD66A9', '#CEC8C8', '#747272' ]
      figure
        div(
          style="background-color:"+clr
        )
        figcaption #{clr}

  hr
  h2 Кнопки
  hr
  h2 Поля ввода
  hr
  h2 Вкладки
  hr
  h2 Пункты меню

  .flex
    ol.m_auto
      li(
        v-for="item in ARR"
      )
        N-link.flex.text_x2.mb-3(
          :to="item"
        ) {{item}}

</template>

<script>
const DATA = [
  'authorization',
  // 'config-roles-add-func',
  // 'config-roles-modify',
  'config-roles',
  // 'config-users-add',
  // 'config-users-modify',
  // 'config-users-role',
  'config-users',
  // 'profile-edit',
  'profile',
  // 'user-role',
  'web-my-orders',
]
export default {
  layout: 'blank',
  data() {
    return {
      ARR: DATA,
    }
  },
}
</script>

<style lang="stylus">

.Index
  background #FFFF


#palette
  display flex
  flex-wrap wrap
  text-align center
  figure
    margin 1em
  div
    width 5em
    height 4em
</style>
