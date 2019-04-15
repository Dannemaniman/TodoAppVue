<template>
    <div>
        <h1 class="main-heading">TODO</h1>
        <h2 class="second-heading">Saker på listan: {{ itemLength }}</h2>
    </div>
    
</template>

<script>
export default {
    props: ['itemLength']
}
</script>

<style>

    .main-heading {
        text-align: center;
        margin-top: 2em;
        font-size: 70px;
        font-weight: 300;
        color: beige;
    }

    .second-heading {
        text-align: center;
        margin: 2em 3em;
        font-weight: 300;
        color: beige;
    }
</style>

