<template>
  <div id = 'homepage'>
      <v-container>
              <v-layout column>
                  <v-carousel>
                      <v-carousel-item
                          src="https://plus.unsplash.com/premium_photo-1683887034146-c79058dbdcb1?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                          cover
                      ></v-carousel-item>

                      <v-carousel-item
                          src="https://images.unsplash.com/photo-1606761568499-6d2451b23c66?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                          cover
                      ></v-carousel-item>

                      <v-carousel-item
                          src="https://images.unsplash.com/photo-1523240795612-9a054b0db644?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                          cover
                      ></v-carousel-item>
                  </v-carousel>
                  </v-layout>
                  <v-layout>
                  <v-container>
                      <v-row align="center" justify="center">
                          <div class="d-flex align-center flex-column">
                              
                             
                              <div class="mt-4 text-subtitle-2">With markup</div>

                              <v-card width="400">
                              <v-card-item>
                                  <v-card-title>{{ componentTitle }}</v-card-title>
                                 
                              </v-card-item>

                              <v-card-text>
                                <v-list
                                :items="courses"
                                item-title="coursename"
                                item-value="id"
                              ></v-list>

                              </v-card-text>
                              </v-card>
                          </div>
                      </v-row>
                  </v-container>
              </v-layout>
          </v-container>
  </div>
</template>

<script>
export default {
  // Properties returned from data() become reactive state
  // and will be exposed on `this`.
  data() {
    return {
      courses:[
        {
          id: 1,
          coursename: 'Financial Economics'
        
        },
        {
          id: 2,
          coursename: 'Psychology'
        },
        {
          id: 3,
          coursename: 'Computer Science'
        },
        {
          id: 4,
          coursename: 'Financial Engineering'
        },
        {
          id: 5,
          coursename: 'Medicine and Surgery'
        },
        {
          id: 6,
          coursename: 'Education'
        },
        {
          id:7,
          coursename: 'Architecture'
        },
        {
          id: 8,
          coursename: 'Forestry'
        },
        {
          id: 9,
          coursename: 'Law'
        },
        {
          id: 10,
          coursename: 'Hospitality and Tourism'
        }
      ],
      componentTitle:'Courses at Strathmore University'
    }
  },

  // Methods are functions that mutate state and trigger updates.
  // They can be bound as event handlers in templates.
  methods: {
    increment() {
      this.count++
    }
  },

  // Lifecycle hooks are called at different stages
  // of a component's lifecycle.
  // This function will be called when the component is mounted.
  mounted() {
    console.log(`The initial count is ${this.count}.`)
  }
}
</script>