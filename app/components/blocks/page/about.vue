<template>
    <div>
        <section data-bs-version="5.1" class="header1 cid-v0HengyO4j" id="header01-0">
            <div class="container-fluid">
                <div class="row justify-content-center">
                    <div class="col-12 col-md-12 col-lg-8 image-wrapper">
                        <img class="w-100" src="https://placehold.net/9.png" alt="Meeovi Tasks" style="height: 650px; width: 650px !important;">
                    </div>
                    <div class="col-12 col-lg col-md-12">
                        <div class="text-wrapper align-left">
                            <h1 class="mbr-fonts-style mb-4 display-2">
                                <strong>{{ about?.name }}</strong>
                            </h1>
                            <p class="mbr-text mbr-fonts-style mb-4 display-7" v-dompurify-html="about?.content"></p>
                            <div>
                                <createList />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
    import createList from '#social/app/components/blocks/partials/listBtn.vue'

    defineProps({
        about: {
            type: Object,
            required: true,
        }
    })
</script>