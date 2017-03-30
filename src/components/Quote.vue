<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <button @click="deleteQuote(quote)">X</button>
                <p>{{ quote }}</p>
            </div>
        </div>

        </div>
    </div>
</template>

<script>
    export default {
        props: ['quote', 'deleteQuote']
    }
</script>

<style scoped>
    .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
    }

    .quote {
        cursor: pointer;
    }
    button {
        font-family: sans-serif;
        float: right;
        font-size: 10px;
    }
</style>