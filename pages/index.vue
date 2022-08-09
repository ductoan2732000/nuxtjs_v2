<template>
  <b-form>
    <b-card>
      <b-form-group
        id="fieldset-1"
        label="Enter your name"
        label-for="input-1"
        valid-feedback="Thank you!"
        :invalid-feedback="invalidFeedback"
        :state="state"
      >
        <b-form-input
          id="input-1"
          v-model="name"
          :state="state"
          trim
        ></b-form-input>
      </b-form-group>
    </b-card>
  </b-form>
</template>

<script lang="ts">
export default {
  name: 'IndexPage',
}
</script>
