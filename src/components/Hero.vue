<template>
    <div class="hero">
      <transition name="fade" appear>
        <h1 class="hero-title" v-html="settings.hero_title" />
        </transition>
        <h2 class="hero-subtitle" v-html="settings.hero_subtitle" />
        <g-link class="hero-cta" to="/contact">Say Hi 👋</g-link>
        
    </div>
</template>

<script>
export default {
  data() {
    return {
      settings: require("../../data/theme.json")
    }
  }
}
</script>

<style>
.fade-enter-active {
  transition: opacity .5s;
}

.fade-enter {
  opacity: 0;
}
.hero {
    text-align: left;
    /* width: 480px; */
    max-width: 100%;
    margin: 0 auto;
    padding: 4rem 0 8rem 0;
}

.hero-title {
    font-size: 6rem;
    font-weight: 700;
    padding: 0;
    margin: 0 0 1rem 0;
}
.hero-title p,
.hero-subtitle p {
    margin: 0;
    padding: 0;
}
.hero-subtitle {
    width: 480px;
    font-size: 1.15em;
    font-weight: 400;
    line-height: 1.68;
    padding: 0;
    margin: 0;
    opacity: 0.6;
    margin-bottom: 1.5rem;
}
.hero-cta {
  font-size: 1.5rem;
    opacity: 0.8;
  text-decoration: none;
  background-color: rgb(243, 228, 91);
  color: #333;
  padding: 10px 15px;
  transition: box-shadow 300ms ease-in-out;
}
.hero-cta:hover {
box-shadow: rgba(143, 129, 0, 0.1) -5px 4px 8px;
}
</style>
