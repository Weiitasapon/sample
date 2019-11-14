<template>
  <v-layout>
    <v-flex class="text-center">
      <img
        src="../assets/img/Asset1.png"
        alt="Vuetify.js"
        class="mb-5"
      >
      <blockquote class="blockquote">
        &#8220;The future of para-rubber industrials&#8221;
        <footer>
          <small>
            <em>&mdash;Weii Tasapon</em>
          </small>
        </footer>
      </blockquote>

  </v-card>
      <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="./"
          >
            Back
          </v-btn>
          <v-btn
            color="green"
            nuxt
            to="/about"
          >
            About
          </v-btn>
        </v-card-actions>
    </v-flex>
  </v-layout>
</template>
