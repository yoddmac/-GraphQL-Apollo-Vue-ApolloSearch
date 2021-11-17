<template>
  <div>
    <ViewAppBar />
    <ViewInputSearch />
  </div>
</template>

<script>
import ViewAppBar from "./viewAppBar"
import ViewInputSearch from "./viewInputSearch"
export default {
    name: "mainView",
    components: {
        ViewAppBar,
        ViewInputSearch
  },
}
</script>

<style>

</style>