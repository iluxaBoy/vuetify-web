
<template>
  <v-app class="px-4">
    <v-main class="box pa-lg-10 pa-6">
      <TopCard class="mb-7" />
      <TopCardInfo class="mb-7" />
      <SubSec class="mb-7" />
      <SubInfo class="mb-7" />
      <BottInfo class="mb-7" />
      <div class="text-center mb-5 font-weight-bold text-medium-emphasis">
        Exchange © 2023
      </div>
    </v-main>
  </v-app>
</template>

<script setup>
import TopCard from "./components/TopCard.vue"
import TopCardInfo from "./components/TopCardInfo.vue";
import SubSec from "./components/SubSec.vue";
import SubInfo from "./components/SubInfo.vue";
import BottInfo from "./components/BottInfo.vue";
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');

*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

.container {
  margin: auto;
  max-width: 1216px;
}

.v-app {
  background-color: black;
}

.top-bar {
  margin-bottom: 38px;
  width: 100%;
  height: 92px;
  background-color: #fff;
}

@media (max-width: 1280px) {
  .container {
    max-width: 1000px;
  }
}

@media (max-width: 1280px) {
  .v-app {
    padding: 26px;
  }
}
</style>