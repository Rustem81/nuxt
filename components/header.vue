<template>
    <header>
        <nav>

            <ul>

                <li>
                    <nuxt-link to="/">Главная</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/recipes">Рецепты</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/about">О нас</nuxt-link>
                </li>
            </ul>
        </nav>
    </header>
</template>


<script>
    import AppLogo from '~/components/AppLogo.vue'
    export default{
        AppLogo

    }
</script>

<style scoped>
    header{
        width: 100%;
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: darkorchid;
    }
ul{
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
}
    li{
        margin: 0 10px;
    }
    a{
        text-decoration: none;
        color: white;
    }

</style>