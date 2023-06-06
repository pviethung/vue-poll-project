<template>
  <v-toolbar>
    <v-container>
      <v-row align="center">
        <h1 class="text-h4 font-weight-bold">Poll</h1>
        <div class="d-flex justify-center align-center pl-4">
          <v-btn variant="text"> Button </v-btn>
        </div>
      </v-row>
    </v-container>
  </v-toolbar>
  <div class="ma-5"></div>

  <v-container>
    <v-row justify="center">
      <v-col cols="8">
        <div class="text-center mb-8">
          <h2 class="text-h4 font-weight-bold">Create a Poll</h2>
          <p>Complete the below fields to create your poll.</p>
        </div>
        <v-form @submit.prevent>
          <v-text-field
            v-model.trim="firstName"
            variant="underlined"
            label="First name"
          ></v-text-field>
          <p>
            {{ firstName }}
          </p>
          <v-btn :prepend-icon="mdiPlus" variant="plain" class="d-flex align-center"
            >Add description or image</v-btn
          >

          <v-select
            class="w-50"
            label="Voting type"
            :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']"
            variant="underlined"
          ></v-select>

          <div class="my-4"></div>
          <p :style="{ opacity: 0.6 }">Answer Options</p>
          <v-text-field variant="underlined" label="Option 1"></v-text-field>
          <v-text-field variant="underlined" label="Option 2"></v-text-field>
          <v-btn :prepend-icon="mdiPlus"> Add option </v-btn>

          <v-divider class="my-8"></v-divider>

          <div>
            <p>Settings</p>
            <v-container>
              <v-row justify="center">
                <v-col>
                  <v-checkbox
                    label="Allow selection of multiple options"
                    color="info"
                    value="info2"
                    hide-details
                  ></v-checkbox>
                  <v-checkbox
                    label="Require participants' names
"
                    color="info"
                    value="info2"
                    hide-details
                  ></v-checkbox>
                </v-col>
                <v-divider vertical></v-divider>

                <v-col>
                  <p :style="{ opacity: 0.6 }">Voting restrictions</p>
                  <v-select
                    :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']"
                    variant="underlined"
                    value="Colorado"
                  ></v-select>

                  <div class="my-4"></div>
                  <p :style="{ opacity: 0.6 }">Strict checking</p>
                  <v-checkbox
                    label="Require participants' names
"
                    color="info"
                    value="info2"
                    hide-details
                  ></v-checkbox>
                </v-col>
              </v-row>
            </v-container>
          </div>

          <v-divider class="my-8"></v-divider>

          <v-btn class="w-25 mr-4 bg-primary"> Create poll </v-btn>
          <v-btn class="w-25"> Save as draft </v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { mdiPlus } from "@mdi/js";
import { ref } from "vue";

const _c = 1;

const firstName = ref("");
</script>

<style scoped></style>
