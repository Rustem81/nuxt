<template>

    <section class="single-recipe">
        <h1>{{ recipes.title }}</h1>
        <div>
            <img class="recipe-img" :src="recipes.thumbnail" :alt="recipes.title">
        </div>
        <p>{{recipes.descriptionText}}</p>
    </section>
</template>

<script>
    export default {

        asyncData(context){
            return new Promise((resolve, reject) => {
                setTimeout(()=>{
                    resolve({
                        recipes:[
                            {
                                id:"1",
                                title: "Пицца",
                                previewText:"Суппер итальянская Пицца!!!",
                                descriptionText:"Наиполнейшее описание, Полное описание подробнейшее",
                                thumbnail:"https://c.pxhere.com/photos/30/0f/pizza_drink_food-954587.jpg!d"

                            },
                            {
                                id:"2",
                                title: "Азия",
                                previewText:"Восточная еда от узбека!!!",
                                descriptionText:"Наиполнейшее описание, Полное описание подробнейшее",
                                thumbnail:"https://upload.wikimedia.org/wikipedia/commons/thumb/c/c1/Indian-Food-wikicont.jpg/800px-Indian-Food-wikicont.jpg"

                            },
                            {
                                id:"3",
                                title: "Азия",
                                previewText:"Восточная еда от узбека!!!",
                                descriptionText:"Наиполнейшее описание, Полное описание подробнейшее",
                                thumbnail:"https://upload.wikimedia.org/wikipedia/commons/thumb/c/c1/Indian-Food-wikicont.jpg/800px-Indian-Food-wikicont.jpg"

                            },
                        ].find(el=> el.id=== context.params.id)

                    })
                },1500)
            })

        },
    }


</script>

<style scoped>
    .single-recipe{
        display: flex;
        justify-content: center;
        flex-flow: column;
        align-items: center;
        text-align: center;
        padding: 30px;
    }
    .recipe-img{
        width: 100%;
        border: 5px solid #ccc;
        box-shadow: 0 2px 2px #aaa;

    }
</style>