<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm8
      md6
    >
      <v-card>
        <v-card-title class="headline">
          Title
        </v-card-title>
        <v-card-text>
          <p>parrafo1.</p>
          <p>parrafo2.</p>
          <p>parrafo3.</p>
          <div class="text-xs-right">
            <em><small>&mdash; Algo </small></em>
          </div>
          <hr class="my-3">
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Boton
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>
