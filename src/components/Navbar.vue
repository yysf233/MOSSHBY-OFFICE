<template>
  <div>
    <vs-navbar style="border-radius: 0%;background-color: rgba(67,67,68);">
      <template #left>
        <vs-button flat icon style="margin-right: 20px" class="menu-btn" @click="activeSidebar = !activeSidebar">
          <i class='bx bx-menu'></i>
        </vs-button>
        <router-link to="/" class="navbar-link">
          <h3>
            <img src="../images/毛衫与白LOGO.png" alt="">
          </h3>
          <!-- <img src="../images/毛衫与白LOGO.png" alt=""> -->
        </router-link>
      </template>
      <vs-navbar-item v-for="(link, index) in links" :key="index" :active="active.name === link.name"
        :to="active.name === link.name ? null : link.url" style="color: #fff;font-size: 20px;">
        {{ link.name }}
      </vs-navbar-item>
      <template #right>
        <vs-navbar-item>
          <vs-switch style="background:#fff;" @click="changeTheme()">
            <template #on>
              <i class='bx bxs-sun'></i>
            </template>
            <template #off>
              <i class='bx bxs-moon'></i>
            </template>
          </vs-switch>
        </vs-navbar-item>
      </template>
    </vs-navbar>
    <vs-sidebar v-model="activeItem" :open.sync="activeSidebar">
      <template #logo>
        <h3>
          <img src="../images/毛衫与白LOGO.png" alt="">
        </h3>
      </template>
      <vs-sidebar-item v-for="(link, index) in links" :key="index" :to="link.url" :id="link.name">
        {{ link.name }}
      </vs-sidebar-item>
    </vs-sidebar>
  </div>
</template>

<script>
let Config = null
try {
  Config = require('@/../posts/data/config.json')
} catch (e) {
  Config = require('@/defaults/config.json')
}

export default {
  name: 'Navbar',
  data: () => {
    return {
      config: Config.config,
      activeItem: 'Home',
      activeSidebar: false,
      dark: false,
      links: [
        {
          name: '主页',
          url: '/'
        },
        {
          name: '关于我们',
          url: '/posts'
        },
        {
          name: 'Projects',
          url: '/projects'
        },
        {
          name: 'Links',
          url: '/links'
        },
        {
          name: 'Tags',
          url: '/tags'
        },
        {
          name: 'About',
          url: '/about'
        }
      ]
    }
  },
  methods: {
    // changeTheme: function () {
    //   if (this.dark) {
    //     document.getElementsByTagName('body')[0].setAttribute('vs-theme', 'light')
    //     this.dark = false
    //   } else {
    //     document.getElementsByTagName('body')[0].setAttribute('vs-theme', 'dark')
    //     this.dark = true
    //   }
    // }
  },
  computed: {
    active: function () {
      const cur = this.$route.path
      var ret = {
        name: null,
        url: null
      }
      for (var i = 0; i < this.links.length; i++) {
        if (this.links[i].url === cur) ret = this.links[i]
      }
      return ret
    }
  }
}
</script>
<style scoped>


.vs-navbar-content {
  position: static;
}

h3 {
  width: 60px;
  margin: 0;
}

img {
  width: 300%;
  margin-left: 20%;
  margin-top: -48px;
  margin-bottom: -48px;
}

.off .bxs-moon:before {
  content: " 中 ";
  color: black;
}

.on .bxs-sun:before {
  content: "俄";
}
</style>