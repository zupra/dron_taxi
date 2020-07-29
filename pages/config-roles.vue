<template lang="pug">
.Page
  .Logo DRON TAXI

  .Grid
    .Nav
      .Nav_item(
        v-for="item in ['Профиль', 'Упр. пользователями', 'Упр. ролями']"
      ) {{item}}
      

    .Main
      h1 Управление ролями
      .Main_body
        .flex
          input(
            placeholder="Системное имя"
          )
          | &emsp;
          input(
            placeholder="Наименование"
          )


      table.my-3.table_hovered
        tr
          each _,i in Array(5)
            th thead_#{i+1}
        each _,i in Array(12)
          tr
            each _,i in Array(5)
              td data_#{i+1}



</template>

<style lang="stylus"></style>
