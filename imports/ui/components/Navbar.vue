<template>
    <ul class="nav">
        <li v-for="link in links" :key="link.id">
          <a :href="link.url" target="_blank">{{link.title}}</a>
        </li>
    </ul>
</template>

<script>
import Links from '../../api/collections/Links'

export default {
  data() {
    return {
      title: "",
      url: "",
    }
  },
  meteor: {
    $subscribe: {
      'links': [],
    },
    links () {
      return Links.find({})
    },
  },
  methods: {
    submit(event) {
      event.preventDefault()
      Meteor.call('createLink', this.title, this.url, (error) => {
        if (error) {
          alert(error.error)
        } else {
          this.title = ''
          this.url = ''
        }
      })
    }
  },
}
</script>