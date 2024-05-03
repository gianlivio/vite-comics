<script>
export default {
    data() {
        return {

        }
    }
}
</script> 

<template>
    <div class="header-container">
    <div class="header-logo">
        <img src="../assets/img/dc-logo.png" alt="">
    </div>
    <ul class="nav-list">
            <li><a href="/characters">Characters</a></li>
            <li><a href="/comics">Comics</a></li>
            <li><a href="/movies">Movies</a></li>
            <li><a href="/tv">TV</a></li>
            <li><a href="/games">Games</a></li>
            <li><a href="/collectibles">Collectibles</a></li>
            <li><a href="/videos">Videos</a></li>
            <li><a href="/fans">Fans</a></li>
            <li><a href="/news">News</a></li>
            <li><a href="/shop">Shop</a></li>
        </ul>
    </div>
    <div class="header-banner">
        <h3>--> content goes here <--</h3>
    </div>
    <div class="main-container">
        <ul class="feature-list">
            <li>
                <img src="../assets/icons/digital-comics.svg" alt="Digital Comics">
                <span>Digital Comics</span>
            </li>
            <li>
                <img src="../assets/icons/merchandise.svg" alt="DC Merchandise">
                <span>DC Merchandise</span>
            </li>
            <li>
                <img src="../assets/icons/subscription.svg" alt="Subscription">
                <span>Subscription</span>
            </li>
            <li>
                <img src="../assets/icons/shop-locator.svg" alt="Comic Shop Locator">
                <span>Comic Shop Locator</span>
            </li>
            <li>
                <img src="../assets/icons/power-visa.svg" alt="DC Power Visa">
                <span>DC Power Visa</span>
            </li>
        </ul>
    </div>
   
</template>

<style scoped lang="scss">
    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    .header-container {
        @include flex(row, space-between, center);
        margin: 2em 10em;
    }

   .header-logo {
    text-align: center;
   }

   ul {
    @include flex(row, center, center);
    list-style-type: none;
    gap: 1em;

    a {
    text-decoration: none;
    color: $text-color;

    &:hover {
        color: $primary-color;
    }
   }
   }

   .header-banner {
    background-color: $dark-gray;


    h3 {
    color: $light-gray;
    margin-left: 6em;
    padding: 3em;
    }

   }


   

</style>