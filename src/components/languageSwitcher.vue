<template>

    <select v-if="$localesList" tabindex="0" @change="changelocale($event)">
  
      <template v-for="(item,key) in $localesList">
        <option v-bind:key="key" :selected="item == $locale" v-bind:value="item">
          <template v-if="item == 'en'">English</template>
          <template v-if="item == 'ru'">Русский</template>
          <!-- {{item}} -->
        </option>
      </template>

    </select>

</template>

<script>

export default {

  methods: {
    changelocale(event) {

        console.log(event.target.value)

        // get chosen locale
        let lang = event.target.value

        //update locale in options
        this.$setLocale(lang)

        //redirect to page with chosen locale
        let newpath = this.$tp(this.$route.path, lang)
        // this.$router.push(newpath) < - this doesn't work for some reason
        window.location.href = newpath

    }
  }

}

</script>