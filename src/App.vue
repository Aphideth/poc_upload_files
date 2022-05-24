<template>
  <v-app>
   <h1>My Librairy</h1>
   <v-card width="600" class="pa-md-4 mx-lg-auto">
    <h2>Add document</h2>
    
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-text-field
      v-model="name"
      :rules="nameRules"
      label="Name1"
      required
    ></v-text-field>
     <v-text-field
      v-model="name"
      :rules="nameRules"
      label="Name2"
      required
    ></v-text-field>
     <v-text-field
      v-model="name"
      :rules="nameRules"
      label="Name3"
      required
    ></v-text-field>
     <v-text-field
      v-model="name"
      :rules="nameRules"
      label="Name4"
      required
    ></v-text-field>
     <v-text-field
      v-model="name"
      :rules="nameRules"
      label="Name5"
      required
    ></v-text-field>
            <v-textarea
          name="input-7-1"
          label="Description"
          value="Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta dolor explicabo quam natus vitae, nemo, ipsa debitis non voluptate repellat porro, exercitationem voluptatibus incidunt. Asperiores dolorem esse voluptas necessitatibus mollitia.
"         
        ></v-textarea>
        <v-combobox
          v-model="select"
          :items="items"
          label="Document type"
          multiple
          chips
        ></v-combobox>
  <v-file-input
    show-size
    counter
    multiple
    label="File input"
  ></v-file-input>
    <v-btn
      :disabled="!valid"
      color="primary"
      class="mr-4"
      @click="validate"
    >
      Validate
    </v-btn>

  </v-form>
 </v-card>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
    
  },

   data () {
      return {
        select: ['Type 1'],
        items: [
          'Type 1',
          'Type 2',
          'Type 3',
          'Type 4',
        ],
      }
    },
}
</script>
