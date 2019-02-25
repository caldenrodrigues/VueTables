<template lang="html">
  <div id="app">
    <v-app id="inspire">
      <v-container style="max-width: 600px;">
        <v-timeline dense clipped>
        <v-timeline-item
          color="amber darken-4"
          fill-dot
          right
        >
        <v-card>
          <v-card-title class="amber darken-4">
            <!--v-icon
              dark
              size="42"
              class="mr-3"
            >
              mdi-magnify
            </v-icon-->
            <h2 class="display-1 white--text font-weight-light">Supplier</h2>
          </v-card-title>
          <v-container>
            <v-layout>
              <v-flex xs10>
                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit.
              </v-flex>
              <v-flex xs2>
                <v-icon size="64">mdi-calendar-text</v-icon>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-timeline-item>

          <!--v-slide-x-transition
            group
          >
            <v-timeline-item
              v-for="event in timeline"
              :key="event.id"
              class="mb-3"
              color="pink"
              small
            >
              <v-layout justify-space-between>
                <v-flex xs7 v-text="event.text"></v-flex>
                <v-flex xs5 text-xs-right v-text="event.time"></v-flex>
              </v-layout>
            </v-timeline-item>
          </v-slide-x-transition>

          <v-timeline-item
            class="mb-4"
            hide-dot
          >
            <span>TODAY</span>
          </v-timeline-item-->

          <v-timeline-item
            class="mb-3"
            icon-color="grey lighten-2"
            small
          >
            <v-layout justify-space-between>
              <v-flex xs7>
                <v-btn small color="primary" dark @click="salesDialog = true">Sales Order</v-btn>
                This order was Placed.
              </v-flex>
              <v-flex xs5 text-xs-right>15:26 EDT</v-flex>
            </v-layout>
          </v-timeline-item>

          <!-- Dialog for Sales Order-->
          <v-dialog
          v-model="salesDialog"
          max-width="290"
        >
          <v-card>
            <v-card-title class="headline">Sales Order</v-card-title>

            <v-card-text>
              Let Google help apps determine location. This means sending anonymous location data to Google, even when no apps are running.
            </v-card-text>

            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn
                color="green darken-1"
                flat="flat"
                @click="salesDialog = false"
              >
                OK
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>

          <v-timeline-item
            class="mb-3"
            small
          >
            <v-layout justify-space-between>
              <v-flex xs7>
                <v-chip
                  class="white--text ml-0"
                  color="purple"
                  label
                  small
                >
                  APP
                </v-chip>
                Digital Downloads fulfilled 1 item.
              </v-flex>
              <v-flex xs5 text-xs-right>15:25 EDT</v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item
            class="mb-3"
            color="grey"
            small
          >
            <v-layout justify-space-between>
              <v-flex xs7>
                Order confirmation email was sent to John Leider (john@vuetifyjs.com).
              </v-flex>
              <v-flex xs5 text-xs-right>15:25 EDT</v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item
            class="mb-3"
            hide-dot
          >
            <v-btn
              class="mx-0"
              color="white"
            >
              Resend Email
            </v-btn>
          </v-timeline-item>

          <v-timeline-item
            class="mb-3"
            color="grey"
            small
          >
            <v-layout justify-space-between>
              <v-flex xs7>
                A $15.00 USD payment was processed on PayPal Express Checkout
              </v-flex>
              <v-flex xs5 text-xs-right>15:25 EDT</v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item
        color="blue accent-4"
        fill-dot
        right
      >
        <v-card>
            <v-card-title class="blue accent-4">
            <v-icon
              dark
              size="42"
              class="mr-3"
            >
              mdi-magnify
            </v-icon>
            <h2 class="display-1 white--text font-weight-light">Manufacturer</h2>
          </v-card-title>
          <v-container>
            <v-layout>
              <v-flex xs10>
                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit.
              </v-flex>
              <v-flex xs2>
                <v-icon size="64">mdi-calendar-text</v-icon>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-timeline-item>

        </v-timeline>
      </v-container>
    </v-app>
  </div>
</template>

<script>
export default {
  name: "ProductChain",
  data() {
    return {
      salesDialog: false,
    }
  },
}
</script>

<style lang="css" scoped>
</style>
