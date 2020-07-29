/*
<template lang="pug">
.Page
  img(
    :src="require(`~/static/img/flying-taxi.jpg`)"
  )
</template>
*/

<template lang="pug">
.Page.flex
  .authorization

  .Logo DRON TAXI


  form
    h2 АВТОРИЗАЦИЯ

    label Логин
      input(
        placeholder="Ввведите логин"
      )

    label Пароль
      input(
        placeholder="Ввведите пароль"
      )

    .flex.y_center.my-3
      span
        input(
          type="checkbox"
        )
        | Запомнить

      button.btn_blue Войти
    .flex
      button.btn_green Регистрация

</template>

<style lang="stylus">





.authorization
  position fixed
  z-index -1
  left 0
  top 0
  width 100%
  height 100vh
  background url('~static/img/flying-taxi.jpg') no-repeat center/cover;
  // mix-blend-mode: overlay;
  // filter: opacity(0.5);
  opacity .5



form
  margin auto 0 auto 2em
  width 300px
</style>
