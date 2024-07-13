<template>
    <div class="main-container w-100" :style="{height: deviceHeight + 'px'}" >
      <div class="w-100 boxex-1 bg-indigo":style="{height:boxex1Height + 'px'}" ></div>
      <div class="w-100 boxex-2":style="{height:boxex2Height + 'px'}" >
        <v-form>
            <v-container class="pa-0">
                <v-row no-gutters>
                <v-col cols="12" >
                    <v-sheet class="pa-1">
                    <p class="text-center font-weight-bold text-h6 text-blue mb-3">Enter Closing Details SF-AA-0020</p>

                    <v-row no-gutters>
                        <v-col cols="5" >
                            <v-sheet class="pa-1">
                                <v-text-field
                                    v-model="loannumber"
                                    :counter="10"
                                    :rules="loannumberRules"
                                    label="Loan_Number:"
                                    placeholder="SF-AA-0020"
                                    hide-details
                                    required
                                    class="w-100"
                                    ></v-text-field>
                            </v-sheet>
                        </v-col>
                        <v-col cols="7" >
                            <v-sheet class="pa-1">
                                <v-text-field
                                    v-model="loantyps"
                                    :counter="10"
                                    :rules="loantypeRules"
                                    label="Loan Type:"
                                    placeholder="Gold"
                                    hide-details
                                    required
                                    class="w-100"
                                    ></v-text-field>
                            </v-sheet>
                        </v-col>
                        <v-col cols="5" class="pa-0" >
                            <v-sheet class="pa-1">
                                <v-date-input label="Loan Date:" prepend-icon=""></v-date-input>
                            </v-sheet>
                        </v-col>
                        <v-col cols="7" >
                            <v-sheet class="pa-1">
                                <v-text-field
                                    v-model="loanvalue"
                                    :counter="10"
                                    :rules="loanvalueRules"
                                    label="Loan value:"
                                    placeholder="0000"
                                    hide-details
                                    required
                                    class="w-100"
                                    ></v-text-field>
                            </v-sheet>
                        </v-col>
                        </v-row>

                    </v-sheet>
                </v-col>

                <v-col cols="12" >
                    <v-sheet class="pa-1">
                        <v-row no-gutters>
                            <v-col cols="5">
                                <v-sheet class="pa-1 d-flex align-end" >
                                    <v-date-input label="Last Date:" prepend-icon=""></v-date-input>
                                </v-sheet>
                            </v-col>
                            <v-col cols="7">
                                <v-sheet class="pa-1" >
                                <v-text-field
                                    v-model="nan"
                                    :counter="10"
                                    :rules="nanRules"
                                    
                                 
                                    hide-details
                                    required
                                    class="w-100"
                                    ></v-text-field>
                                    <v-btn class="bg-indigo text-white" @click="sheet = !sheet" block>Total 7946.2</v-btn>
                                </v-sheet>
                            </v-col>
                            </v-row>
                    </v-sheet>
                </v-col>

                <v-col cols="12" class="pa-1" >
                    <v-sheet>
                        <v-row no-gutters class="pa-0">
                            <v-col cols="5" class="pa-0">
                                <v-sheet class="pa-0" >

                                    <v-col cols="12" class="pa-0">
                                        <v-sheet class="pa-1" >
                                        <span>Collected Extra:</span><br>
                                        <span>19955.10:</span>
                                        </v-sheet>
                                    </v-col>

                                    <v-col cols="12" class="pa-0 mt-2">
                                        <v-sheet class="pa-1" >
                                            <span>Intrest:</span><br>
                                            <span>19955.10:</span>
                                        </v-sheet>
                                    </v-col>

                                    <v-col cols="12" class="pa-0 mt-2">
                                        <v-sheet class="pa-1" >
                                            <span>Book Value:</span><br>
                                            <span>7555.10:</span>
                                        </v-sheet>
                                    </v-col>

                                </v-sheet>
                            </v-col>
                            <v-col cols="7">
                                <v-sheet class="pa-0" >
                                    
                                    <v-col cols="12" class="pa-0">
                                        <v-sheet class="pa-1" >
                                            <v-text-field
                                                v-model="nan"
                                                :counter="10"
                                                :rules="nanRules"
                                                placeholder="-5600.00"
                                            
                                                hide-details
                                                required
                                                class="w-100"
                                                ></v-text-field>
                                        </v-sheet>
                                    </v-col>

                                    <v-col cols="12" class="pa-0">
                                        <v-sheet class="pa-1" >
                                            <v-text-field
                                                v-model="nan"
                                                :counter="10"
                                                :rules="nanRules"
                                                placeholder="-5600.00"
                                            
                                                hide-details
                                                required
                                                class="w-100"
                                                ></v-text-field>
                                        </v-sheet>
                                    </v-col>

                                    <v-col cols="12" class="pa-0">
                                        <v-sheet class="pa-1" >
                                            <v-text-field
                                                v-model="nan"
                                                :counter="10"
                                                :rules="nanRules"
                                                placeholder="000"
                                            
                                                hide-details
                                                required
                                                class="w-100"
                                                ></v-text-field>
                                        </v-sheet>
                                    </v-col>

                                </v-sheet>
                            </v-col>
                            </v-row>
                    </v-sheet>
                </v-col>
                
                <v-col cols="12" >
                    <v-sheet class="pa-1">
                        <v-row no-gutters>
                            <v-col cols="5">
                                <v-sheet class="pa-1" >
                                <span>Office Book:</span><br>
                                <span>0.000:</span>
                                </v-sheet>
                            </v-col>
                            <v-col cols="7">
                                <v-sheet class="pa-1" >
                                    <v-text-field
                                    v-model="nan"
                                    :counter="10"
                                    :rules="nanRules"
                                    placeholder="000"
                                
                                    hide-details
                                    required
                                    class="w-100"
                                    ></v-text-field>
                                </v-sheet>
                            </v-col>
                            </v-row>
                    </v-sheet>
                </v-col>
                
                </v-row>
            </v-container>
        </v-form>
      </div>
  
      <div class="w-100 d-flex ga-3 pa-4 align-center" :style="{height:boxex3Height + 'px'}" >
        <div class="text-center w-100 pa-0" >
    <v-btn
      class="bg-indigo"
      text="7946.2"
      @click="sheet = !sheet"
      block
    ></v-btn>
    <v-bottom-sheet v-model="sheet" class="pa-0">
      <v-card class="pa-0" :style="{height: tabHeight + 'px'}">
        <v-card-text>
          <v-btn variant="text" @click="sheet = !sheet" icon="$cancel"></v-btn>
          <br>
          <br>
          <div>
    <v-card class="pa-0">
      <v-tabs v-model="tab" align-tabs="center" stacked>
        <v-tab
          value="tab-1"
          :class="{'bg-blue text-white': tab === 'tab-1'}"
        >
          Week<br>Details
        </v-tab>

        <v-tab
          value="tab-2"
          :class="{'bg-blue text-white': tab === 'tab-2'}"
        >
          Months<br>20.40
        </v-tab>

        <v-tab
          value="tab-3"
          :class="{'bg-blue text-white': tab === 'tab-3'}"
        >
          Interest<br>Rs.123.40
        </v-tab>

        <v-tab
          value="tab-4"
          :class="{'bg-blue text-white': tab === 'tab-4'}"
        >
          Collect<br>Rs.6892.40
        </v-tab>
      </v-tabs>

      <v-tabs-window v-model="tab">
        <v-tabs-window-item value="tab-1">
          <v-card >
            <v-card-text>
              <v-card rounded="0"  flat>
    <v-window v-model="onboarding">
      <v-window-item :value="1">
        <v-card class="d-flex justify-center align-center">
          <div class="w-100 d-flex flex-column ga-2">
            <div class="w-100" style="border: 2px solid blue">
              <div class="w-100 d-flex justify-space-between">
                <span>Loan Item</span>
                <span class="d-flex justify-center"><v-icon class="text-yellow" icon="mdi-circle"></v-icon>3.500g</span>
              </div>
              <div class="w-100">
                <span>Ring</span><br>
                <span>Ring</span>
              </div>
            </div>
            <div class="w-100 d-flex justify-center align-center pa-10" style="border: 2px solid blue">
              <span>Picture-1</span>
            </div>
          </div>
        </v-card>
      </v-window-item>
      <v-window-item :value="2">
        <v-card class="d-flex justify-center align-center">
          <div class="w-100 d-flex flex-column ga-2">
            <div class="w-100" style="border: 2px solid blue">
              <div class="w-100">
                <p class="text-black font-weight-bold text-h">Name & Address</p>
                <p>ABCDE, 37, Main Street,<br> Thiruvaiyar, Thanjavur<br>Thanjavur<br>Thanjavur</p>
              </div>
      
            </div>
            <div class="w-100 d-flex justify-center align-center pa-10" style="border: 2px solid blue">
              <span>Picture-2</span>
            </div>
          </div>
        </v-card>
      </v-window-item>
      <v-window-item :value="3">
        <v-card class="d-flex justify-center align-center">
          <div class="w-100 d-flex flex-column ga-2">
            <div class="w-100" style="border: 2px solid blue">
              <div class="w-100">
                <p class="text-black font-weight-bold text-h">ID Proof Details</p>
                <p>Aadhaar<br>XXXX XXXX 1234</p>
              </div>
      
            </div>
            <div class="w-100 d-flex justify-center align-center pa-10" style="border: 2px solid blue">
              <span>Picture-3</span>
            </div>
          </div>
        </v-card>
      </v-window-item>
      <!-- Add more v-window-item elements as needed -->
    </v-window>

    <v-card-actions class="d-flex justify-center" >
      <v-item-group v-model="onboarding" class="text-center" mandatory >
        <v-item v-for="n in length" :key="`btn-${n}`" v-slot="{ isSelected, toggle }" :value="n">
          <v-btn :variant="isSelected ? 'outlined' : 'text'" icon="mdi-record" @click="toggle"></v-btn>
        </v-item>
      </v-item-group>
    </v-card-actions>
  </v-card>
            </v-card-text>
          </v-card>
        </v-tabs-window-item>

        <v-tabs-window-item value="tab-2">
          <v-card >
            <v-card-text>
              <h3>Months</h3>
              <p>Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
            </v-card-text>
          </v-card>
        </v-tabs-window-item>

        <v-tabs-window-item value="tab-3">
          <v-card >
            <v-card-text>
              <h3>Interest</h3>
              <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            </v-card-text>
          </v-card>
        </v-tabs-window-item>

        <v-tabs-window-item value="tab-4">
          <v-card >
            <v-card-text>
              <h3>Collect</h3>
              <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            </v-card-text>
          </v-card>
        </v-tabs-window-item>
      </v-tabs-window>
    </v-card>
  </div>  </v-card-text>
                    </v-card>
                    </v-bottom-sheet>
                </div>
          <div class="w-100"><nuxt-link to="/dashboard" style="text-decoration: none;"><v-btn class="bg-green text-white" block>Submit & Close</v-btn></nuxt-link></div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        deviceWidth: 0,
        deviceHeight: 0,
        boxex1Height: 0,
        boxex2Height: 0,
        boxex3Height: 0,
        tabHeight:0,
        sheet: false,
        tab: 'tab-1',
        length: 3,
        onboarding: 1,
        length:3
      
  
      };
    },
    mounted() {
      this.updateDeviceDimensions(); // Initial call to set dimensions on component mount
      window.addEventListener('resize', this.updateDeviceDimensions); // Listen for window resize events
    },
    beforeDestroy() {
      window.removeEventListener('resize', this.updateDeviceDimensions); // Clean up: remove resize event listener
    },
    methods: {
      updateDeviceDimensions() {
        this.deviceWidth = window.innerWidth; // Update device width
        this.deviceHeight = window.innerHeight; // Update device height
  
        // Calculate heights for each boxex based on percentages
        this.boxex1Height = Math.floor(this.deviceHeight * 0.05); // 6% of device height
        this.boxex2Height = Math.floor(this.deviceHeight * 0.90); // 88% of device height
        this.boxex3Height = Math.floor(this.deviceHeight * 0.05); // 6% of device height
        this.tabHeight = Math.floor(this.deviceHeight * 0.70);
       
      },

  
    }
  };
  </script>
  
  <style scoped>
  
  
  .bg-blue {
  background-color: blue !important;
}

.text-white {
  color: white !important;
}
.text-center {
  text-align: center;
}
  </style>
  