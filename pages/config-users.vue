<template lang="pug">
div
  h1 Управление пользователями
  .Main_body
    .flex

      .flex_col
        img(
          style="width: 120px;"
          :src="require(`~/static/img/clear-prof.png`)"
        )
        button.mt-5.btn_blue Обновить


      .ml-5
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

        label Дата рождения
          //- input(
          //-   type="date"
          //- )
          InpDate

        //-
          .flex
            label Пол
              input(
                type="date"
              )


      .ml-5
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

    .mt-3.flex.x_end
      button.btn_green Сохранить
      | &emsp;
      button.btn_blue Отмена

</template>

<script>
import InpDate from '~/components/InpDate.vue'
export default {
  components: {
    InpDate,
  },
}
</script>
