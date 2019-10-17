<template>
    <section class="recipes">
        <Recipe
            thumbnail="https://assets3.thrillist.com/v1/image/2797371/size/tmg-article_default_mobile.jpg"
            title="Delicious Hamburger"
            id="1"
            previewText="Awesome Hamburger!"
        />
        <Recipe 
            thumbnail="https://www.medicalnewstoday.com/content/images/articles/324/324956/close-up-of-a-plate-of-food.jpg"
            title="Delicious vegetables"
            id="2"
            previewText="Awesome vegetables"
        />
    </section>
</template>

<script>
import Recipe from '@/components/Recipe'
export default {
    components: {
        Recipe
    },
    asyncData() {

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