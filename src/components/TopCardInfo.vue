<template>
    <div class="container">
        <v-card class="px-lg-10 py-lg-7
            px-4 py-5
            d-sm-block d-flex 
            justify-center
            rounded-xl">
            <div class="d-flex flex-column flex-sm-row">
                <div>
                    <v-img style="width: 294px; height: 208px; border-radius: 15px;" src="@/assets/image4.png"
                        lazy-src="@/assets/image4.png" />
                </div>
                <div class="ma-md-8 ma-4 mt-sm-0 mt-2">
                    <v-card-title class="title font-weight-bold mb-5 pa-0">Open Campus</v-card-title>
                    <v-card-text class="pa-0 mb-9">A Web3 Education Protocol to tokenize educational
                        content -
                        first adopted by Tiny Tap</v-card-text>
                    <div class="d-flex flex-wrap ml-lg-5">
                        <v-btn elevation="0" color="#DFDFDF" class="px-lg-5 px-mg-5 mb-3 text-capitalize">
                            <v-icon icon="mdi-link-variant" />
                            <span class="ml-1">
                                Web
                            </span>
                        </v-btn>
                        <v-btn elevation="0" color="#DFDFDF" class="ml-4 px-lg-5 px-mg-5 mb-3 text-capitalize">
                            <v-icon icon="mdi-file" />
                            <span class="ml-1">
                                Whitepaper
                            </span>
                        </v-btn>
                        <v-btn elevation="0" color="#DFDFDF" class="ml-md-4 px-lg-5 px-mg-5 mb-3 text-capitalize">
                            <v-icon icon="mdi-text-box" />
                            <span class="ml-1">
                                Details
                            </span>
                        </v-btn>
                        <v-btn elevation="0" color="#DFDFDF" class="ml-4 px-lg-5 px-mg-5 mb-3">
                            <v-icon icon="mdi-frequently-asked-questions" />
                            <span class="ml-1">
                                FAQ
                            </span>
                        </v-btn>
                    </div>
                </div>
            </div>
            <div v-if="!isMobile()" class="d-flex align-center mt-13 ml-6">
                <v-card elevation="0" style="background-color: #FDD835" class="px-5 rounded-xl py-3 pb-8">
                    <v-card-title class="text-subtitle-1 font-weight-medium pa-0">Calculate maximum
                        investment</v-card-title>
                    <v-row class="ml-0 mt-0">
                        <v-text class="mr-3">2023-09-08</v-text>
                        <v-divider class="line" vertical></v-divider>
                        <v-text class="ml-3">03:00</v-text>
                    </v-row>
                </v-card>

                <v-icon size="65" color="#FDD835" icon="mdi-menu-right" />

                <v-card elevation="0" style="background-color: #FDD835" class="px-5 rounded-xl py-3 pb-8">
                    <v-card-title class="text-subtitle-1 font-weight-medium pa-0">Fixing USDT</v-card-title>
                    <v-row class="ml-0 mt-0 mr-2">
                        <v-text class="mr-3">2023-09-12</v-text>
                        <v-divider class="line" vertical></v-divider>
                        <v-text class="ml-3">14:00</v-text>
                    </v-row>
                </v-card>

                <v-icon size="65" color="#FDD835" icon="mdi-menu-right" />

                <v-card elevation="0" style="background-color: #FDD835" class="px-5 rounded-xl py-3 pb-8">
                    <v-card-title class="text-subtitle-1 font-weight-medium pa-0">Distribution of tokens</v-card-title>
                    <v-row class="ml-0 mt-0 mr-2">
                        <v-text class="mr-3">2023-09-15</v-text>
                        <v-divider class="line" vertical></v-divider>
                        <v-text class="ml-3">01:00</v-text>
                    </v-row>
                </v-card>

                <v-icon size="65" color="#FDD835" icon="mdi-menu-right" />

                <v-card elevation="0" style="background-color: #FDD835" class="px-5 rounded-xl py-3 pb-8">
                    <v-card-title class="text-subtitle-1 font-weight-medium pa-0">Distribution</v-card-title>
                    <v-row class="ml-0 mt-0 mr-2">
                        <v-text class="mr-3">2023-09-16</v-text>
                        <v-divider class="line" vertical></v-divider>
                        <v-text class="ml-3">10:00</v-text>
                    </v-row>
                </v-card>
            </div>
        </v-card>
    </div>
</template>

<script setup>
import { useDisplay } from 'vuetify'

const { width } = useDisplay()

function isMobile() {
    return width.value <= 1280;
}
</script>

<style scoped lang="scss">
.title {
    font-size: 40px;
}

.v-divider {
    margin-top: 3px;
    height: 19px;
}

@media (max-width: 1280px) {
    .title {
        font-size: 24px;
    }

    .v-btn {
        font-size: 14px;
    }
}
</style>