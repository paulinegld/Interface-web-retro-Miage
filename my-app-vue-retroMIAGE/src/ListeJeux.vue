<template>
  <v-data-table
    :headers="headers"
    :items="listejeux"
    class="elevation-1"
  >

    <template slot="items" slot-scope="props">

      <td>{{ props.item.name }}</td>
      <td class="text-xs-left">{{ props.item.console}}</td>


    </template>
  </v-data-table>
</template>

<script>
    export default {
        name: "ListeJeux",
      data () {
        return {
          headers: [
            {
              text: 'Nom du jeux',
              align: 'center',
              sortable: true,
              value: 'name'
            },
            {text: 'Console', value: 'console', sortable: true}
          ],
          listejeux: [{
            name: 'Super Mario Bross',
            console: 'Wii',
          },
            {
              name: 'Mario Kart',
              console: 'Wii',
            },
            {
              name: 'Nintendogs',
              console: 'Nintendo DS',
            },
            {
              name: 'Animal Crossing',
              console: 'Nintendo DS',
            },
            {
              name: 'Metroid',
              console: 'Nintendo DS',
            }
          ]
        }
      }
    }
</script>

<style scoped>

</style>
