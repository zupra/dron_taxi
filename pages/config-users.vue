<template lang="pug">
.Page
  .Logo DRON TAXI

  .Grid
    .Nav
      .Nav_item(
        v-for="item in ['Профиль', 'Упр. пользователями', 'Упр. ролями']"
      ) {{item}}
      

    .Main
      h1 Мой профиль

      .Main_body

        .flex

          div
            img(
              style="width: 120px;"
              :src="require(`~/static/img/clear-prof.png`)"
            )


          .ml-4

            label Фамилия
              input(
                placeholder="Фамилия"
              )

            label Имя
              input(
                placeholder="Имя"
              )

            label Отчество
              input(
                placeholder="Отчество"
              )

          .ml-4
            label Email
              input(
                placeholder="Email"
              )

            label Телефон
              input(
                placeholder="Телефон"
              )


            label Пароль
              input(
                placeholder="Пароль"
              )

            label Подтверждение пароля
              input(
                placeholder="Подтверждение пароля"
              )

        br
        br
        button.btn_green Сохранить
        | &emsp;
        button.btn_green Отмена

</template>
