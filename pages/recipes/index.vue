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
import Recipe from '@/components/Recipe'
import { resolve, reject } from 'q'
export default {
    components: {
        Recipe
    },
    asyncData() {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipes: [
                        {
                            id: "1",
                            title: "Delicious hamburger",
                            previewText: "Awesome hamburger",
                            thumbnail: "https://assets3.thrillist.com/v1/image/2797371/size/tmg-article_default_mobile.jpg"
                        },
                        {
                            id:"2",
                            title: "Delicious vegetables",
                            previewText: "Awesome vegetables",
                            thumbnail: "https://www.medicalnewstoday.com/content/images/articles/324/324956/close-up-of-a-plate-of-food.jpg"
                        }
                    ]
                })
            }, 1500)
        })
    }
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