<template>
  <header>
    <ul>
      <li @click="showBio">Bio</li>
      <li @click="showWork">Work</li>
      <li @click="showContact">Contact</li>
    </ul>
    <div>
      <img src="../assets/logo-a-mini.png" />
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
header {
    height: 25px;
    width: 100%;
    position: fixed;
    top: 0;
}
ul{
    margin: 0;
}
li{
    display: inline;
    margin: 0;
}

</style>
