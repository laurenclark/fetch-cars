<template>
    <main role="main" id="app">
        <a href="https://github.com/laurenclark/fetch-cars">View on Github</a>
        <Cars />
    </main>
</template>

<script>
    import Cars from "./components/Cars.vue";

    export default {
        name: "app",
        components: {
            Cars
        }
    };
</script>

<style lang="scss">
    * {
        box-sizing: border-box;
    }
    body {
        padding: 1rem;
        font-family: Avenir, Roboto, Helvetica, san-serif;
    }

    main {
        max-width: 500px;
        margin: 0 auto;
    }
    article {
        margin: 1rem 0;
    }

    @supports (display: grid) {
        main {
            max-width: 10000px;
            margin: 0;
        }
        article {
            margin: 0;
        }
        .container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 2fr));
            grid-gap: 1.3rem;
        }
    }
</style>