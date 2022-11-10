<template>
    <main>
        <section id="jumbotron"></section>
        
        <section id="secondary-nav">
            <div class="container">
                
            </div>
        </section>
    </main>
</template>

<script>

</script>

<style scoped lang="scss">
@import "../assets/scss/partials/variables.scss";

main {
    color: $main_color;
    background-color: #1c1c1c;

    .container {
        position: relative;
        padding: 50px 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }

    #jumbotron {
        background-image: url("../assets/img/jumbotron.jpg");
        background-repeat: no-repeat;
        background-position: top center;
        background-size: cover;
        height: 400px;
    }

    #secondary-nav {
        background-color: $DcBlue;
    }
}
</style>