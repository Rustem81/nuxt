<template>
  <section class="recipes">

      <Recipe
              v-for="recipe in recipes"
              :key="recipe.id"
              :thumbnail="recipe.thumbnail"
              :title="recipe.title"
              :id="recipe.id"
              :previewText="recipe.previewText"
      />




  </section>
</template>

<script>
   import Recipe from '~/components/Recipe.vue'
   import axios from 'axios'
    export default {
        components:{
            Recipe
        },
        asyncData(){
            return new Promise((resolve, reject) => {
                setTimeout(()=>{
                    resolve({
                        recipes:[
                            {
                                id:"1",
                                title: "Пицца",
                                previewText:"Суппер итальянская Пицца!!!",
                                thumbnail:"https://c.pxhere.com/photos/30/0f/pizza_drink_food-954587.jpg!d"

                            },
                            {
                                id:"2",
                                title: "Азия",
                                previewText:"Восточная еда от узбека!!!",
                                thumbnail:"https://upload.wikimedia.org/wikipedia/commons/thumb/c/c1/Indian-Food-wikicont.jpg/800px-Indian-Food-wikicont.jpg"

                            },
                            {
                                id:"3",
                                title: "Азия",
                                previewText:"Восточная еда от узбека!!!",
                                thumbnail:"https://upload.wikimedia.org/wikipedia/commons/thumb/c/c1/Indian-Food-wikicont.jpg/800px-Indian-Food-wikicont.jpg"

                            },
                        ]

                    })
                },1500)
            })

        },
    };
</script>
<style scoped>
  .recipes {
      display: flex;
      flex-flow: row wrap;
      justify-content: center;
      align-items: center;
  }
</style>
