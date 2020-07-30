<template lang="pug">
div
  h1 Управление ролями
  .Main_body

    .flex.x_sb
      .flex

        img.mr-3(
          :src="require(`~/static/icon-svg/filter.svg`)"
        )

        input(
          placeholder="Системное имя"
        )
        | &emsp;
        input(
          placeholder="Наименование"
        )

      button.btn_blue.flex.y_center
        img(
          :src="require(`~/static/icon-svg/add-button.svg`)"
        )
        | &nbsp; Добавить

    .flex

      table.mt-4.flex_1
        tbody
          tr
            each _,i in Array(5)
              th thead_#{i+1}
          each _,i in Array(10)
            tr
              each _,i in Array(5)
                td data_#{i+1}

      .ml-5

        h2.mb-1 Роль: Администратор
        .flex
          label Системное имя
            input(
              placeholder="Админ"
            )

          label.ml-4 Наименование
            input(
              placeholder="Администратор"
            )


        .flex
          label Дата начала
            input(
              type="date"
            )

          label.ml-4 Дата окончания 
            input(
              type="date"
            )

        .mt-4.flex.x_sb.y_end
          h3 Доступный функционал
          button.btn_blue.flex.y_center
            img(
              :src="require(`~/static/icon-svg/add-button.svg`)"
            )
            | &nbsp; Добавить

        table.mt-3.w_100
          //-
            thead
              tr
                each _,i in Array(2)
                  th thead_#{i+1}
          tbody
            each _,i in Array(3)
              tr
                each _,i in Array(2)
                  if ! i
                    td data_#{i+1}
                  else
                    td.td_buttonGroup
                      img(
                        :src="require(`~/static/icon-svg/delete-grin.svg`)"
                      )



        .flex.mt-3
          button.btn_green Сохранить
          button.btn_blue.ml-3 Отмена

</template>

<style lang="stylus"></style>
