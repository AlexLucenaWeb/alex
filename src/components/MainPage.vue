<template>
  <section>
    <div class="container" @click="animation">
      <div>
        <img alt="Alex logo" src="../assets/alex-animation.gif" id="alexLogo" />
      </div>
      <div class="menu">
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
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  max-height:100vh;
}
.menu{
  font-size: 3rem;
  line-height: 1.5em;
  position: absolute;
  bottom: 40%;
  left: 50%;;
  text-align: left;
}

ul{
    list-style: none;
}
</style>
