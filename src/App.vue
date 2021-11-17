<template>
  <v-app>
    <v-main>
      <MainView/>
    </v-main>
  </v-app>
</template>

<script>
import MainView from './views/mainView';

export default {
  name: 'App',
  components: {
    MainView,
  },

  data: () => ({
    //
  }),
};
</script>
