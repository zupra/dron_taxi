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

      table.my-3
        tbody
          tr
            each _,i in Array(5)
              th thead_#{i+1}
          each _,i in Array(12)
            tr
              each _,i in Array(5)
                td data_#{i+1}

      .ml-5

        h2.my-2 Роль: Администратор
        .flex
          label Системное имя
            input(
              placeholder="Админ"
            )

          label.ml-3 Наименование
            input(
              placeholder="Администратор"
            )


        .flex
          label Дата начала
            input

          label.ml-5 Дата окончания 
            input



        table.my-3
          thead
            tr
              each _,i in Array(3)
                th thead_#{i+1}
          tbody
            each _,i in Array(5)
              tr
                each _,i in Array(3)
                  td data_#{i+1}



</template>

<style lang="stylus"></style>
