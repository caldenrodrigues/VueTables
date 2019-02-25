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
                <pre>
                  Organization Name : Farmer Rocks
                  Address : Some Random Address in nagpur.
                </pre>
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
              <pre>
Payment ID: 1001234
Material Name: Coffee beans
Quantity: 10kg
Amount: 10500
              </pre>
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
                    <v-btn small color="primary" dark @click="packTicket = true">Packing Ticket</v-btn>
                    Order is packed.
                  </v-flex>
                  <v-flex xs5 text-xs-right>18:45 IST</v-flex>
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
                  <v-btn small color="primary" dark @click="shipTicket = true">Shipment Ticket</v-btn>
                  Order has arrived.
                </v-flex>
                <v-flex xs5 text-xs-right>22:45 IST</v-flex>
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
                <pre>
                  Organization Name : Trader Rocks
                  Address : Some Trader Address in nagpur.
                </pre>
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
