<template>
  <div>
    <h1 class="head">Avatar Variation</h1>
    <v-row justify="space-around">
      <v-avatar :color="color" :size="size" :tile="isTile">
        <img src="https://ryocv.online/profile/img/profile.webp" alt="yuuri" />
      </v-avatar>
    </v-row>

    <v-row>
      <v-col cols="12">
        <v-row justify="center">
          <v-col cols="6" md="2">
            <v-select
              v-model="color"
              :items="colorList"
              label="Color"
            ></v-select>
          </v-col>
          <v-col cols="6" md="2">
            <v-select v-model="size" :items="sizeList" label="Size"></v-select>
          </v-col>
          <v-col cols="6" md="2">
            <v-checkbox v-model="isTile" label="Tile"></v-checkbox>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      colorList: ['red', 'blue', 'green', 'yellow', 'orange', 'black', 'white'],
      color: 'red',
      sizeList: ['32', '48', '60', '72', '84', '96'],
      size: '48',
      isTile: false,
    }
  },
}
</script>

<style>
.head {
  text-align: center;
  margin-bottom: 10px;
}
</style>
