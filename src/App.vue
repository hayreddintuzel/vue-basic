<template>
    <div class="container">
        <div class="row mt-5">
            <button class="btn btn-primary" @click="addPreview">+ Add New </button>
        </div>
        <div class="row bordered mt-4">
            <progress-bar :counter="counter"></progress-bar>
        </div>
        <div class="row mt-4 bordered">
            <div class="col-6">
                <app-quote-preview :preview="previewData"></app-quote-preview>
            </div>
            <div class="col-6">
                <textarea class="col-12" rows="10" v-model="previewData"></textarea>
            </div>
        </div>
        <div class="row mt-4 p-1">
            <stored-quotes v-for="preview in previews">{{preview}}</stored-quotes>
        </div>
    </div>
</template>

<script>
    import appQuotePreview from './components/AppQuotePreview.vue';
    import progessBar from './components/ProgressBar.vue';
    import storedQuotes from './components/StoredQuotes.vue';
    export default {
        components: {
            appQuotePreview:  appQuotePreview,
            progressBar: progessBar,
            storedQuotes: storedQuotes
        },
        data() {
            return {
                previewData: "dsadas",
                counter: 0,
                previews: []
            }
        },
        methods: {
            addPreview: function () {
                if (this.counter < 10) {
                    this.counter++;
                    this.previews.push(this.previewData);
                    this.previewData = '';
                }

            }
        }
    }
</script>

<style>
.bordered {
 border: 3px gray solid;
 padding: 15px;
}
</style>
