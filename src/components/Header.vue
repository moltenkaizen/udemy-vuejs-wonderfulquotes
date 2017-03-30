<template>
    <div class="row">
        <div class="col-sm-12">
        <h3>Quotes Added</h3>
        <div class="progress">
            <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" :style="{ width: percentage + '%'}">
                {{ numQuotes }} / {{ maxQuotes }}
              </div>
        </div>
        </div>
        <!--<p>percentage: {{ percentage }}</p>-->
    </div>
</template>

<script>
    export default {
        props: ['numQuotes', 'maxQuotes'],
        computed: {
            percentage() {
                return this.numQuotes / this.maxQuotes * 100
            }
        }
    }
</script>

<style>
</style>