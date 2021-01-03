<template>
  <section class="section">
    <div class="columns is-mobile">
      <div class="column"></div>
      <div class="column is-narrow">
        <b-field label="Spelling Bee Letters">
          <b-input 
            placeholder="7 unique letters" 
            rounded 
            maxlength="7" 
            type="text" 
            v-on:input="boardModified" 
            v-model="board" 
            validation-message="Must be 7 unique lower case letters" 
            pattern="(?:([a-z])(?!.*\1))*" >
          </b-input>
        </b-field>

        <b-field label="Center Letter">
          <b-input 
            placeholder="center letter" 
            rounded 
            maxlength="1" 
            type="text" 
            v-model="centerChar" 
            validation-message="Must be one of the 7 unique letters" 
            v-bind:pattern="centerCharPattern">
          </b-input>
        </b-field>
        <div class="columns is-mobile">
          <div class="column"></div>
          <div class="column">
            <b-button type="is-primary">Solve</b-button>
          </div>
          <div class="column"></div>
        </div>
      </div>
      <div class="column"></div>
    </div>
  </section>
</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'HomePage',

  components: {
    Card
  },

  data() {
    return {
      board: '',
      centerChar: '',
      centerCharPattern: '[]'
    }
  },

  methods: {
    boardModified() {
      this.centerCharPattern = `[${this.board}]`;
    }
  }
}
</script>
