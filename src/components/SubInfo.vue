<template>
    <div class="container">
        <v-card class="rounded-xl py-md-7 px-md-7 py-0 px-0 pb-6 pr-16">
            <v-card-title class="pb-0 mb-md-5 font-weight-medium">Subscription duration</v-card-title>
            <div v-for="id in data" :key="id" class="main mx-md-16 mt-md-13 mx-6 d-flex">
                <v-btn v-if="!isMobile()" class="mt-3" flat icon="" color="#FFF8DB" size="x-large">
                    <v-icon color="#FEDC4A" size="x-large">mdi-check</v-icon>
                </v-btn>
                <v-btn v-if="isMobile()" class="mt-3" flat icon="" color="#FFF8DB" size="x-small">
                    <v-icon color="#FEDC4A">mdi-check</v-icon>
                </v-btn>
                <div class="ml-md-10 ml-3">
                    <v-card-title class="mb-2 font-weight-medium">{{ id.title }}</v-card-title>
                    <v-row class="mb-0 font-weight-medium">
                        <span>{{ id.date }}</span>
                        <v-divider class="mx-3" vertical></v-divider>
                        <span>{{ id.time }}</span>
                    </v-row>
                    <v-card-text v-if="!isMobile()" class="text font-weight-medium text-medium-emphasis">{{ id.text
                    }}</v-card-text>
                </div>
            </div>
        </v-card>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import { useDisplay } from 'vuetify'

const { width } = useDisplay()

function isMobile() {
    return width.value <= 960;
}
const data = ref([
    {
        id: 1,
        title: "Distribution",
        date: "2023-09-08",
        time: "03:00",
        text: "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Suspendisse volutpat tempus risus, eu cursus urna bibendum et.Vestibulum ligula mauris, pharetra non pretium in, scelerisque vitae risus.Lorem ipsum dolor sit amet,consectetur adipiscing elit. Suspendisse volutpat tempus risus, eu cursus urna bibendum et."
    },
    {
        id: 2,
        title: "Subscription start",
        date: "2023-09-08",
        time: "03:00",
        text: "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Suspendisse volutpat tempus risus, eu cursus urna bibendum et.Vestibulum ligula mauris, pharetra non pretium in, scelerisque vitae risus.Lorem ipsum dolor sit amet,consectetur adipiscing elit."
    },
    {
        id: 3,
        title: "Billing period",
        date: "2023-09-08",
        time: "03:00",
        text: "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Suspendisse volutpat tempus risus, eu cursus urna bibendum et.Vestibulum ligula mauris, pharetra non pretium in, scelerisque vitae risus."
    },
    {
        id: 4,
        title: "Final distribution of tokens",
        date: "2023-09-08",
        time: "03:00",
        text: "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Suspendisse volutpat tempus risus, eu cursus urna bibendum et.Vestibulum ligula mauris, pharetra non pretium in, scelerisque vitae risus.Vestibulum ligula mauris, pharetra non pretium in, scelerisque vitae risus."
    },
]);
</script>

<style scoped lang="scss">
.v-card {

    .v-card-title {
        font-size: 32px;
    }
}

.main {
    .v-card-title {
        padding-left: 0;
        font-size: 24px;
    }

    div {
        .v-row {
            margin-left: 0;
            font-size: 18px;
        }

        .v-card-text {
            padding-left: 0;
            font-size: 18px;
        }
    }
}

@media (max-width: 960px) {
    .v-card {
        // display: flex;
        // flex-direction: column;
        // padding: 16px 12px;

        .v-card-title {
            margin-bottom: 0px;
            font-size: 20px;
        }

        div {
            .v-card-title {
                font-size: 16px;
            }

            .v-row {
                font-size: 12px;
            }
        }
    }
}
</style>