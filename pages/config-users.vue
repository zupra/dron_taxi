<template lang="pug">
div
  h1 Управление пользователями


  //- .Main_body

  .HERE_tabs
    .tabLabels
      .tabLabels_Item(
        v-for="(tab,idx) in ['Список', 'Личные данные', 'Роли']",
        :class="{curr:idx==TAB}",
        @click="TAB = idx"
      ) {{tab}}

    transition-group(
      class="TAB_content" name="tab"
    )
      .TAB(:key="0" v-show="TAB == 0")
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
            //-
        table.w_100.mt-4
          tbody
            tr
              each _,i in Array(5)
                th thead_#{i+1}
            each _,i in Array(10)
              tr
                each _,i in Array(5)
                  if i === 4
                    td.td_buttonGroup.center
                      img(
                        :src="require(`~/static/icon-svg/delete-grin.svg`)"
                      )
                  else
                    td data_#{i+1}

      .TAB(:key="1" v-show="TAB == 1")
        Profile
      .TAB(:key="2" v-show="TAB == 2")
        h1 Роли

</template>

<script>
import Profile from '~/components/Profile.vue'
export default {
  components: {
    Profile,
  },
  data() {
    return {
      TAB: 0,
    }
  },
}
</script>
