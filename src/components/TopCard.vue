<template>
    <div class="container">
        <v-card class="rounded-xl">
            <div class="py-md-5 px-md-10 py-3 px-4 d-flex align-center justify-space-between">
                <div class="d-flex align-center">
                    <v-btn size="small" class="mr-6" style="color: #757575;" icon="" variant="outlined">
                        <v-icon size="35" style="color: #757575;">
                            mdi-arrow-left-thin
                        </v-icon>
                    </v-btn>
                    <v-divider vertical></v-divider>
                    <v-card-subtitle v-if="!isMobile()" class="sub-text ml-12">
                        LAUNCHPAD / DETAILS / PROJECT / 1
                    </v-card-subtitle>
                </div>
                <div>
                    <span class="card-text font-weight-medium">
                        Open Campus
                    </span>
                </div>
                <v-card-title class="text-white">Open Capmus</v-card-title>
                <v-btn size="small" color="#2196F3"
                    class="pending px-4 text-white rounded-lg font-weight-light">PENDING</v-btn>
            </div>
            <div class="blur overflow-hidden">
                <v-img class="top-img" lazy-src="@\assets\image2.png" cover />
            </div>
        </v-card>
    </div>
</template>

<script setup>
import { useDisplay } from 'vuetify'

const { width } = useDisplay()

function isMobile() {
    return width.value <= 725;
}
</script>

<style scoped lang="scss">
.v-card {
    .sub-text {
        font-size: 20px;
    }

    .card-text {
        font-size: 18px;
    }

    .blur {
        background-color: #4C1920;

        .v-img {
            height: 248px;
            filter: blur(18px);
        }
    }

    .v-card-title {
        position: absolute;
        left: 20px;
        top: 108px;
        font-size: 32px;
        z-index: 3;
    }

    .pending {
        position: absolute;
        right: 40px;
        top: 118px;
        z-index: 3;
    }
}


@media (max-width: 860px) {
    .v-card {
        .card-title {
            font-size: 20px;
        }

        .v-card-title {
            top: 70px;
            left: 0px;
        }

        .pending {
            padding: 3px 18px;
            right: 10px;
            top: 80px;
        }
    }
}
</style>