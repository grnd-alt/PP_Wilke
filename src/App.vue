<template>
  <meta name="viewport" content="width=device-width,initial-scale=1.0">
  <div id="nav">
    <router-link to ="/about">about</router-link>
    <router-link to ="/">home</router-link>
    <!-- <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link> -->
  </div>
  <router-view v-slot="{ Component }">
    <transition name="fade" mode="out-in">
      <component :is="Component"  :animate="animate" v-if="isload"/>
    </transition>
  </router-view>
    <bottombar/>
</template>
<script>
import bottombar from './components/bottombar.vue'
export default ({
  data () {
    return {
      isload: false,
      animate: false,
      im: new Image()
    }
  },
  components: {
    bottombar
  },
  watch: {
    $route (to, from) {
      window.scrollTo(0, 0)
    }
  },
  methods: {
    CheckComplete (count) {
      if (!this.im.complete) setTimeout(this.CheckComplete.bind(count++), 100)
      else {
        this.isload = true
        if (count !== 0) this.animate = true
      }
    }
  },
  mounted () {
    this.im.src = require('@/assets/Chris-unge-Goerdeller.jpg')
    this.CheckComplete(0)
    // CheckComplete(im)
    console.log(this.im.src)
    // console.log(this.im.complete + 'here')
  }
})
</script>

<style>
body,#app,html{
    margin:0;
    height:100vh;
}
#app >* {
  margin:8px;
}
#app{
  display:flex;
  flex-direction:column;
}
:root{
  --maincolor:black;
  --white:rgb(255,255,255);
  --contrast:white;
}
.fade-enter-from{
  opacity:0;
  transform:translateX(-50%);
  /* transform:translateX(-200%); */
}
.fade-enter-to{
  opacity:1;
  transform:translateX(0%);
  /* transform:translateX(100%); */
  /* transition:all 1s; */
}
.fade-enter-active{
  transition:all 0.5s;
}

.fade-leave-from{
  opacity:1;
  transform:translateX(0%);
}
.fade-leave-to{
  opacity:0;
  transform:translateX(50%);
}
.fade-leave-active{
  transition:all 0.5s;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav{
  text-align: right;
  margin-block:1rem;
}

#nav a{
  font-weight: 900;
  /* border-radius:0.3rem; */
  padding-inline:0.5rem;
  cursor:pointer;
  font-size:1.15rem;
  /* background:var(--white); */
  color:var(--maincolor);
  text-decoration: none;
  padding-inline:0.7rem;
  padding-block:0.15rem;
  margin-inline: 0.rem;
  position:relative;
}
#nav a::after{
  border-radius:0.3rem;
  position:absolute;
  box-sizing: border-box;
  content:"";
  left:0;
  top:0;
  width:100%;
  height:100%;
  background: var(--maincolor);
  transform:scaleX(0);
  transform-origin:center;
  transition:transform 200ms ease-in;
  z-index:-1;
}
#nav:last-child{
  margin-right:-1rem;
}
#nav a:hover,
#nav a:focus{
  color:var(--white);
  transition-duration:200ms;
}
#nav a:hover::after,
#nav a:focus::after{
  transform-origin: center;
  transform: scaleX(1);
  transition-duration: 200ms;
}
#nav .router-link-exact-active{
  color:var(--white);
}
#nav .router-link-exact-active::after{
  transform: scaleX(1);
}
</style>
