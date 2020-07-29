/*
<template lang="pug">
.Page
  

  img(
    :src="require(`~/static/img/flying-taxi.jpg`)"
  )
</template>
*/

<template lang="pug">

//- .authorization
//-   h1 HELLO authorization
.Page

  .Logo DRON TAXI


  form.m-3
    h2 АВТОРИЗАЦИЯ

    label Логин
      input(
        placeholder="Ввведите логин"
      )

    label Пароль
      input(
        placeholder="Ввведите пароль"
      )

    .flex
      input(
        type="checkbox"
      )

      button Войти

    .button Регистрация

</template>

<style lang="stylus">





.authorization
  position fixed
  width 100%
  height 100vh
  background url('~static/img/flying-taxi.jpg') no-repeat center/cover;
  // mix-blend-mode: overlay;
  // filter: opacity(0.5);
  opacity .5



form
  width 300px
</style>
