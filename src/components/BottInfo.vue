<template>
    <div class="container">
        <v-card class="rounded-xl py-md-7 px-md-10 pb-md-16 py-4 px-3">
            <div class="top-sec">
                <v-row no-gutters class="mb-16">
                    <v-col>
                        <v-card-title class="pt-0 font-weight-medium">Open Campus</v-card-title>
                        <v-card-text class="text-medium-emphasis text-body-1 font-weight-medium">A Web3 Education Protocol
                            to tokenize educational content - first adopted by Tiny Tap</v-card-text>
                    </v-col>
                    <div class="d-md-block d-none">
                        <v-icon icon="mdi-instagram" color="#808080" size="38" />
                        <v-icon class="ml-4" icon="mdi-twitter" color="#808080" size="38" />
                        <v-icon class="ml-4" icon="mdi-earth" color="#808080" size="38" />
                    </div>
                </v-row>
            </div>
            <div class="mid-sec mb-15">
                <v-card-title class="text-h6 py-0 font-weight-medium mb-5">Project Introduction</v-card-title>
                <v-card-text class="text-body-1 font-weight-medium text-medium-emphasis">
                    Open Campus Protocol is a web3 education protocol for tokenizing educational content by enabling
                    teachers and creators to monetize the content that they created. Its mission is to ensure teachers’
                    contribution to the society is recognised and provide a global, alternative education system for
                    learners worldwide.
                    TinyTap is Open Campus Protocol’s first adopter, it is known for its no-code authoring platform that has
                    produced over 250k interactive lessons to date. It is a top 10 grossing kids mobile application on the
                    App Store and Google Play with 9 million+ families and 100k+ content creators.
                    EDU is the native token of the Open Campus ecosystem (including TinyTap), where EDU can be used on the
                    Open Campus platform and participate in Open Campus DAO governance proposals to guide the direction of
                    the protocol development.
                </v-card-text>
            </div>
            <v-card-title class="text-h6 py-0 font-weight-medium mb-8">Open Campus Token Sale and Economics</v-card-title>
            <v-timeline truncate-line="both" side="end">
                <v-timeline-item v-for="id in data" :key="id" dot-color="yellow-darken-1" size="xs-small" fill-dot>
                    <template v-slot:opposite>
                        <span class="text-right">{{ id.name }}</span>
                    </template>
                    <span class="font-weight-bold">{{ id.info }}</span>
                </v-timeline-item>
            </v-timeline>
        </v-card>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const data = ref([
    {
        id: 1,
        name: "Hard Cap",
        info: "2.500.000 USD"
    },
    {
        id: 2,
        name: "Total Token Supply",
        info: "1.000.000.000 EDU"
    },
    {
        id: 3,
        name: "Initial Circulating Supply",
        info: "14.50% of Total Token Supply"
    },
    {
        id: 4,
        name: "Public Sale Token Price",
        info: "0.05 USD (price in BNB will be determined prior to the start of subscription)"
    },
    {
        id: 5,
        name: "Tokens Offered",
        info: "50.000.000 EDU"
    },
    {
        id: 6,
        name: "Hard Cap Per User",
        info: "15.000 USD (price in BNB will be determined prior to the start of subscription)"
    },
    {
        id: 7,
        name: "Token Sale Vesting Period",
        info: "No lockup"
    },
    {
        id: 8,
        name: "Token Type",
        info: "TRC20"
    },
    {
        id: 9,
        name: "Token Distribution",
        info: "After the end of token sale"
    }
]);
</script>

<style scoped lang="scss">
.v-row {
    .v-card-title {
        font-size: 32px;
        margin-bottom: 12px;
    }
}

.v-timeline {
    font-size: 16px;
    max-width: 659px;
    margin-left: 350px;
}

@media (max-width: 1280px) {
    .v-timeline {
        margin-left: 245px;
        max-width: 520px;
    }
}

@media (max-width: 1100px) {

    .v-timeline {
        font-size: 14px;
        margin: auto;
        max-width: 314px;
    }

    .v-row {
        .v-card-title {
            font-size: 20px;
        }
    }
}
</style>