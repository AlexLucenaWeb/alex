<template>
  <section>
    <div class="container" @click="animation">
      <div>
        <img alt="Alex logo" src="../assets/alex-animation.gif" id="alexLogo" />
      </div>
      <div>
        <ul>
          <li>Bio</li>
          <li>Work</li>
          <li>Contact</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
container {
  display: flex;
}
</style>
