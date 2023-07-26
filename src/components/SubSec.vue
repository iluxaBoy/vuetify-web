<template>
    <div class="container">
        <v-card class="rounded-xl py-md-7 px-md-7 px-4 py-6">
            <v-row class="top-sec mx-auto d-flex flex-md-row flex-column align-start align-md-center justify-space-between">
                <v-col v-for="id in data" :key="id" class="pa-0 mb-3" cols="auto">
                    <v-card-subtitle class="pa-0 mb-1">{{ id.name + ":" }}</v-card-subtitle>
                    <span class="pa-0 text-subtitle-1 font-weight-medium">{{ id.text }}</span>
                </v-col>
            </v-row>
            <div class="bott-sec">
                <div class="rounded mx-auto mt-7">
                    <v-card-subtitle class="pa-0 text-center">Max. per user</v-card-subtitle>
                    <v-card-text class="pa-0 font-weight-medium text-center">300000 EDU = 45,8429 BNB (=14294
                        USD)</v-card-text>
                </div>
            </div>
        </v-card>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const data = ref([
    {
        id: 1,
        name: "Type",
        text: "Subscription"
    },
    {
        id: 2,
        name: "Distribution",
        text: "50 000 000, 000 EDU"
    },
    {
        id: 3,
        name: "Price",
        text: "1 EDU = 0.00015281BNB"
    },
    {
        id: 3,
        name: "Min. attachments",
        text: "0.1 BNB"
    }
]);
</script>

<style scoped lang="scss">
.bott-sec {
    div {
        padding: 8px 144px;
        max-width: 669px;
        background-color: #DFDFDF;
        font-size: 18px;
    }
}

@media (max-width: 900px) {

    // .v-col {
    //     margin-top: 26px;
    // }

    .v-col:first-of-type {
        margin-top: 0;
    }

    .bott-sec div {
        padding: 9px 44px;
        max-width: 314px;
        font-size: 16px;
    }
}

@media (max-width: 570px) {
    .top-sec {
        align-content: flex-start;
    }
}
</style>