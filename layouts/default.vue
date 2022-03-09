<template>
  <div>
    <v-spacer />
    <the-header layout="right">
      <template #logo>
        <nuxt-link to="/" class="logo">
          <img src="/images/logo-new.png" alt="luke electric nj logo" />
        </nuxt-link>
      </template>
      <template #menu>
        <the-menu
          layout="right"
          :primary-nav="headerLinks"
          :secondary-nav="footerLinks"
        >
          <template #logo>
            <nuxt-link to="/" class="logo">
              <img src="/images/logo-new.png" alt="luke electric nj logo" />
            </nuxt-link>
          </template>
          <template #component> <i class="fa-light fa-bolt" /> </template>
        </the-menu>
      </template>
    </the-header>
    <v-spacer />
    <main>
      <nuxt keep-alive />
    </main>
    <v-spacer />
    <the-footer
      company-name="Luke Electric"
      :navigation="[
        {
          url: 'tel:+1-908-246-8546',
          text: '(908) 246-8546',
        },
        {
          url: 'mailto:Lukeelectric13@gmail.com',
          text: 'Email Us',
        },
        {
          url: 'https://www.google.com/maps/place/Luke+Electric+LLC/@40.7005691,-74.9635502,15z/data=!4m5!3m4!1s0x0:0x935b5fafd5a5016a!8m2!3d40.7005691!4d-74.9635502',
          text: 'Directions',
        },
      ]"
    >
      <template #logo>
        <nuxt-link to="/" class="logo">
          <img src="/images/logo-new.png" alt="luke electric nj logo" />
        </nuxt-link>
      </template>
    </the-footer>
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
  mode: 'out-in',
  components: {
    TheFooter: () => import("vue-evolve/src/components/TheFooter"),
    TheHeader: () => import("vue-evolve/src/components/TheHeader"),
    TheMenu: () => import("vue-evolve/src/components/TheMenu")
  },
  data () {
    return {
      data: null
    }
  },
  async fetch() {
    this.data = await this.$storyapi.get(`cdn/stories/global`, {
      version: 'published'
    })
  },
  computed: {
    footerLinks () {
      return this.formatNavigationLinks(this.data?.data.story.content.footer_links)
    },
    headerLinks () {
      return this.formatNavigationLinks(this.data?.data.story.content.header_links)
    }
  },
  methods: {
    formatNavigationLinks (array) {
      if (array){
        return array.map(item => {
          const container = {};
          if(item.link.linktype !== 'story') container.url = item.link.url
          container.text = item.display_name
          if(item.link.linktype === 'story') container.route = item.link.cached_url
          container.type = item.link.linktype === 'story' ? 'nuxt' : 'external'
          return container;
        })
      }
      else {
        return []
      }
    },
  }
}
</script>

<style lang="scss">
.logo,
.logo:active {
  border-bottom: none;

  &:hover {
    border-bottom: none;
  }

  img {
    max-height: 100px;
  }
}

.header .menu {
  ul {
    margin: 0;
  }
  .primary-navigation-item,
  .secondary-navigation-item {
    margin: 0 0 var(--space-2) 0;
  }
}

footer .v-spacer {
  padding: var(--space-1);
}

footer p {
  font-style: italic;
  font-size: var(--font-size-5) !important;
}
</style>