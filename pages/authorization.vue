<template lang="pug">
.Login.flex_col

  N-link.logo(
    to="/"
  ) DRON TAXI


  .Login_form
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
      label.flex_1.flex.y_center
        input(
          type="checkbox"
        )
        | Запомнить

      button.flex_1.btn_blue Войти
    
    button.w_100.btn_green Регистрация

</template>

<script>
export default {
  layout: 'blank',
}
</script>

<style lang="stylus">

.Login
  height 100vh
  color #FFF
  background url('~static/img/flying-taxi_clr.jpg') no-repeat center/cover;
  &_form
    margin auto 0 auto 10vw
    width 300px
</style>
