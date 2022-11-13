<template>
    <ul>
        <li v-for="(comic, index) in comics" :key="index">
            <div class="card"><img :src="comic.thumb" :alt="comic.series" /></div>
            <p class="comic-series">{{ comic.series }}</p>
        </li>
    </ul>
</template>

<script>
    import { ComicsInfo } from '../assets/data/dc-comics';
    export default {
        name: 'Comics',
        data() {
            return {
                comics: ComicsInfo,
            }
        },
        mounted() {
            console.log(this.comics)
        },
    }
</script>



<style scoped lang="scss">
@import "../assets/scss/partials/variables.scss";
#comics {
    ul {
        list-style-type: none;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;

        li {
            margin: 20px 5px;
            width: 200px;
        }

        .card {
            width: 200px;
            height: 200px;
            overflow: hidden;
            
        }
            .card img{
                object-fit: cover;
                transition: 0.5s;
            }

           .card img:hover {
                transform: rotate(6deg) scale(1.2);
            }

        p {
            padding: 20px 0;
        }

        .comic-series {
            text-transform: uppercase;
        }
    }
}
</style>