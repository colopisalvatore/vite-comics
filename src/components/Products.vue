<template>
    <ul>
        <li v-for="(product, index) in products" :key="index">
            <img :class="{ resized: product.resized }" :src="('../src/assets/img/' + product.img)" />
            <a :href="product.url">{{ product.text }}</a>
        </li>
    </ul>
</template>

<script>
export default {
    name: "Products",
    data() {
        return {
            products: [
                {
                    img: "buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS",
                    url: "#",
                    resized: true,
                },
                {
                    img: "buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url: "#",
                    resized: false,
                },
                {
                    img: "buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url: "#",
                    resized: false,
                },
                {
                    img: "buy-comics-shop-locator.png",
                    text: "COMIC SHOP LOCATOR",
                    url: "#",
                    resized: true,
                },
                {
                    img: "buy-dc-power-visa.svg",
                    text: "DC POWER VISA",
                    url: "#",
                    resized: false,
                },
            ],
        };
    },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/partials/variables.scss";

ul {
    list-style-type: none;
    display: flex;
    justify-content: space-between;

    li {
        padding: 10px;
        display: flex;     
        align-items: center;

        img {
            width: 50px;
            height: 56px;
            margin-right: 10px;
            color: $main_color;
        }

        img.resized {
            width: 40px;
        }

        a {
            color: $main_color;
            font-weight: bolder;
        }
    }
}
</style>