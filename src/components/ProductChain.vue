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
            <h2 class="display-1 white--text font-weight-light">Raw Material Supplier</h2>
          </v-card-title>
          <v-container>
            <v-layout>
              <v-flex xs10>
                  <h2 class="text-lg-left blue--text text--lighten-1">Organization Name : </h2><h3 class="text-lg-left"> Trader Rocks</h3>
                  <br />
                  <h2 class="text-lg-left blue--text text--lighten-1">Address :</h2><h3 class="text-lg-left"> Some Trader Address in nagpur. <br />Maharastra<br />India</h3>

              </v-flex>
              <v-flex xs2>
                <v-icon size="64">mdi-calendar-text</v-icon>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-timeline-item>

      <v-timeline-item
        class="mb-3"
        icon-color="grey lighten-2"
        small
      >
        <v-layout justify-space-between>
          <v-flex xs7>
            The Order was placed by "Awesome Trader"
          </v-flex>
          <v-flex xs5 text-xs-right>15:26 EDT</v-flex>
        </v-layout>
      </v-timeline-item>

      <v-timeline-item
        class="mb-3"
        icon-color="grey lighten-2"
        small
        hide-dot
      >
        <v-layout justify-space-between>
          <v-flex xs7>
            <v-btn small color="primary" dark @click="salesDialog = true">Sales Order</v-btn>
          </v-flex>
        </v-layout>
      </v-timeline-item>

          <!-- Dialog for Sales Order-->
      <v-dialog
      v-model="salesDialog"
      max-width="290"
    >
      <v-card>
        <v-card-title class="headline text-lg-left blue--text">Sales Order</v-card-title>

        <v-card-text class="text-lg-left">
          <h3>Payment ID: 1001234<br />
          Material Name: Coffee beans<br />
          Quantity: 10kg<br />
          Amount: 10500</h3>
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
        icon-color="grey lighten-2"
        small
      >
        <v-layout justify-space-between>
          <v-flex xs7>
            Order is packed and ready to be shipped.
          </v-flex>
          <v-flex xs5 text-xs-right>18:45 IST</v-flex>
        </v-layout>
      </v-timeline-item>

      <v-timeline-item
        class="mb-3"
        icon-color="grey lighten-2"
        small
        hide-dot
      >
        <v-layout justify-space-between>
          <v-flex xs7>
            <v-btn small color="primary" dark @click="packTicket = true">Packing Ticket</v-btn>
          </v-flex>
        </v-layout>
      </v-timeline-item>

      <!-- Dialog for Sales Order-->
      <v-dialog
        v-model="packTicket"
        max-width="290"
      >
        <v-card>
          <v-card-title class="headline">Packing Ticket</v-card-title>

          <v-card-text>
            <pre>
    Packment ID: 12345
    Material Name: Coffee beans
    Quantity: 10kg
    Delivery Date: 12/02/1999
            </pre>
          </v-card-text>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn
              color="green darken-1"
              flat="flat"
              @click="packTicket = false"
            >
              OK
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>

      <v-timeline-item
        class="mb-3"
        icon-color="grey lighten-2"
        small
      >
        <v-layout justify-space-between>
          <v-flex xs7>
            Order has arrived at "Awesome Place".
          </v-flex>
          <v-flex xs5 text-xs-right>22:45 IST</v-flex>
        </v-layout>
      </v-timeline-item>

      <v-timeline-item
        class="mb-3"
        icon-color="grey lighten-2"
        small
        hide-dot
      >
        <v-layout justify-space-between>
          <v-flex xs7>
            <v-btn small color="primary" dark @click="shipTicket = true">Shipment Ticket</v-btn>
          </v-flex>
        </v-layout>
      </v-timeline-item>

            <!-- Dialog for Sales Order-->
      <v-dialog
        v-model="shipTicket"
        max-width="290"
      >
        <v-card>
          <v-card-title class="headline">Shipment Ticket</v-card-title>

          <v-card-text>
            <pre>
    Shipment ID: 12345
    Material Name: Coffee beans
    Quantity: 10kg
    Holes: false
    Condensation: false
    Insect Activity: false
            </pre>
          </v-card-text>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn
              color="green darken-1"
              flat="flat"
              @click="shipTicket = false"
            >
            OK
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>



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
              <h2 class="display-1 white--text font-weight-light">Trader</h2>
            </v-card-title>
            <v-container>
              <v-layout>

                  <v-flex xs10>
                      <h2 class="text-lg-left blue--text text--lighten-1">Organization Name : </h2><h3 class="text-lg-left"> Trader Rocks</h3>
                      <br />
                      <h2 class="text-lg-left blue--text text--lighten-1">Address :</h2><h3 class="text-lg-left"> Some Trader Address in nagpur. <br>Maharastra<br />India</h3>
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
      packTicket: false,
      shipTicket: false
    }
  },
}
</script>

<style lang="css" scoped>
</style>
