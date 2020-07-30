<template lang="pug">
div
  h1 Профиль
  .Main_body

    Profile

    .flex.mt-5
      div
        h2 Мои поездки
        .flex.mt-3
          img.mr-3(
            :src="require(`~/static/icon-svg/filter.svg`)"
          )

          input(
            placeholder="Место отправления"
          )
          | &emsp;
          input(
            placeholder="Место назначения"
          )
        
        table.mt-4
          tbody
            tr
              each _,i in Array(5)
                th thead_#{i+1}
            each _,i in Array(6)
              tr
                each _,i in Array(5)
                  td data_#{i+1}
      .ml-5
        h2 Новая поездка
        input.my-3(
          placeholder="Откуда"
        )
        input(
          placeholder="Куда"
        )
        label Tранспорт
          select(
            v-model="form.city"
            placeholder="Обязательно"
          )
            option(
              value="NULL"
            ) Выберите транспорт
            option(
              v-for="It in ARR"
              :value="It.val"
            ) {{It.name}}
</template>

<script>
import Profile from '~/components/Profile.vue'
const DATA = [
  { name: 'Эконом', val: '1' },
  { name: 'Бизнес', val: '2' },
  { name: 'Премиум', val: '3' },
]
export default {
  components: {
    Profile,
  },
  data() {
    return {
      ARR: DATA,
      form: {
        city: 'NULL',
      },
    }
  },
}
</script>
