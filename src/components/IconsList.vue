<script>
export default {
    data() {
        return {
            blueBarItems: [
                {
                    image: 'buy-comics-digital-comics.png',
                    title: 'DIGITAL COMICS'
                },
                {
                    image: 'buy-comics-merchandise.png',
                    title: 'DC MERCHANDISE'
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    title: 'SUBSCRIPTION'
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    title: 'COMIC SHOP LOCATOR'
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    title: 'DC POWER VISA'
                }
            ]
        };
    },
    methods: {
        getImageUrl(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        }
    },
};
</script>

<template>
   <section>
    <div class="container">
        <ul>
            <li v-for="item in blueBarItems" :key="item.title">
                <img :src="getImageUrl(item.image)" alt="item.title">
                <h4>{{ item.title }}</h4>
            </li>
        </ul>
    </div>
   </section>
</template>

<style scoped lang="scss">
@use "../style/partials/_variables.scss" as *;
@use "../style/partials/_mixin.scss" as *;

section {
    background-color: $primary-color;
    padding: 3rem 0;
    color: white;

    ul {
        list-style: none;
       @include flex($justify-content: space-evenly);

        li {
            @include flex();
            
            gap: 1rem;
            img {
                height: 50px;

            }

            h4 {
                font-weight:300;
                font-size: 0,8rem;
            }
        }
    }
}

</style>