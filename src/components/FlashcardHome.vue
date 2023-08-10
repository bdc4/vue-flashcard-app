<template>
    <div class="greetings">
      <h3>
        Flashcards {{ baz }}
      </h3>
    </div>
  </template>

  <script>
  import $ from 'jquery'
  export default {
    data () {
        return {
            foo: 'bar'
        }
    },
    computed: {
        baz () {
            return this.getFlashcards()
        }
    },
    methods: {
        getFlashcards () {
            return $.get({
                url: 'https://www.github.com/queryluke/masseffect-5e-data/blob/master/docs/v144/en/powers.json'
            })
        }
    }
  }
  </script>
  