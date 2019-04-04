<template>
  <v-data-table
    :headers="headers"
    :items="listejeux"
    class="elevation-1"
  >

    <template slot="items" slot-scope="props">

      <td>{{ props.item.name }}</td>
      <td class="text-xs-left">{{ props.item.console}}</td>
      <td class="imageDisplay" v-if="props.item.image!=''"><img v-bind:src="props.item.image" width=200></img></td>
      <td v-else><button>Ajouter une image</button></td>

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
            {text: 'Console', value: 'console', sortable: true},
            {
              text: "Image du jeu",
              align: 'center',
              sortable:true
            }
          ],
          listejeux: [{
            name: 'Super Mario Bros',
            console: 'NES',
            image:"src/images/marioB.jpg"
          },
            {
              name: 'Mario Kart Wii',
              console: 'Wii',
              image:""
            },
            {
              name: 'Nintendogs',
              console: 'Nintendo DS',
              image:""
            },
            {
              name: 'Terranigma',
              console: 'Super Nintendo',
              image:"src/images/terranigma.png"
            },
            {
              name: 'Metroid Prime Hunters',
              console: 'Nintendo DS',
              image:""
            }
          ]
        }
      }
    }

</script>

<style scoped>

</style>
