<template>
  <div>
    <h1 style="text-align: center">Alert Variation</h1>
    <v-alert
      v-model="isAlertList[0]"
      :border="border"
      :colored-border="isColoredBorder"
      :dense="isDense"
      :dismissible="isDismissible"
      :prominent="isProminent"
      :text="isText"
      :transition="transition"
      type="success"
    >
      <div v-if="isDisplayTitle" class="title">Title</div>
      success alert.
    </v-alert>
    <v-alert
      v-model="isAlertList[1]"
      :border="border"
      :colored-border="isColoredBorder"
      :dense="isDense"
      :dismissible="isDismissible"
      :prominent="isProminent"
      :text="isText"
      :transition="transition"
      type="info"
    >
      <div v-if="isDisplayTitle" class="title">Title</div>
      info alert.
    </v-alert>
    <v-alert
      v-model="isAlertList[2]"
      :border="border"
      :colored-border="isColoredBorder"
      :dense="isDense"
      :dismissible="isDismissible"
      :prominent="isProminent"
      :text="isText"
      :transition="transition"
      type="warning"
    >
      <div v-if="isDisplayTitle" class="title">Title</div>
      warning alert.
    </v-alert>
    <v-alert
      v-model="isAlertList[3]"
      :border="border"
      :colored-border="isColoredBorder"
      :dense="isDense"
      :dismissible="isDismissible"
      :prominent="isProminent"
      :text="isText"
      :transition="transition"
      type="error"
    >
      <div v-if="isDisplayTitle" class="title">Title</div>
      error alert.
    </v-alert>

    <v-row>
      <v-col cols="12">
        <v-row justify="center">
          <v-col cols="6" md="2">
            <v-select
              v-model="border"
              :items="boderList"
              label="Border"
            ></v-select>
          </v-col>

          <v-col cols="6" md="2">
            <v-checkbox
              v-model="isColoredBorder"
              label="Color Border"
            ></v-checkbox>
          </v-col>

          <v-col cols="6" md="2">
            <v-checkbox v-model="isDense" label="Dense"></v-checkbox>
          </v-col>

          <v-col cols="6" md="2">
            <v-checkbox
              v-model="isDismissible"
              label="Dismissible"
            ></v-checkbox>
          </v-col>
        </v-row>

        <v-row justify="start">
          <v-col cols="6" md="2">
            <span>Display</span>
          </v-col>
          <v-col cols="6" md="2">
            <v-checkbox v-model="isAlertList[0]" label="Success"></v-checkbox>
          </v-col>
          <v-col cols="6" md="2">
            <v-checkbox v-model="isAlertList[1]" label="Info"></v-checkbox>
          </v-col>
          <v-col cols="6" md="2">
            <v-checkbox v-model="isAlertList[2]" label="Warning"></v-checkbox>
          </v-col>
          <v-col cols="6" md="2">
            <v-checkbox v-model="isAlertList[3]" label="Error"></v-checkbox>
          </v-col>
          <v-col cols="6" md="2">
            <v-checkbox v-model="isDisplayTitle" label="Title"></v-checkbox>
          </v-col>
        </v-row>

        <v-row justify="start">
          <v-col cols="6" md="2">
            <span>Decoration</span>
          </v-col>
          <v-col cols="6" md="2">
            <v-checkbox v-model="isProminent" label="Prominent"></v-checkbox>
          </v-col>
          <v-col cols="6" md="2">
            <v-checkbox v-model="isText" label="Text"></v-checkbox>
          </v-col>
          <v-col cols="6" md="2">
            <v-select
              v-model="transition"
              :items="transitionList"
              label="Transition"
            ></v-select>
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
      boderList: ['top', 'right', 'bottom', 'left'],
      border: 'left',
      isColoredBorder: false,
      isDense: false,
      isDismissible: false,
      isAlertList: [true, true, true, true],
      isDisplayTitle: false,
      isProminent: false,
      isText: false,
      transitionList: [
        'scale-transition',
        'fab-transition',
        'fade-transition',
        'scroll-x-transition',
        'scroll-y-transition',
      ],
      transition: 'scale-transition',
    }
  },
}
</script>
