<template>
  <div>
    <v-text-field
        type="text"
        v-model="search"
        placeholder="Recherche"
        filled
        rounded
        dense
    ></v-text-field>
  <v-card align="center" justify="center" class="mx-auto" max-width="344">
    <v-card-title class="justify-center" >
      <p>DB GraphQL / Apollo / Vue</p>
    </v-card-title>
      <v-card-text class="justify-center">
        <div class="apollo" v-for="user in filteredArticles" :key="user.id">{{user.name}}</div>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
import gql from "graphql-tag";
export default {
  name: "InputSearch",
  apollo: {
    users: gql`query {
      users {
        id
        name
        email
      }
    }`,
  },
  data() {
    return {
      search: '',
      users: [],
    }
  },
  computed: {
      filteredArticles() {
        return this.users.filter((element) => {
            return element.name.toLowerCase().includes(this.search.toLowerCase())
        });
      }
  },
}
</script>

<style>

</style>