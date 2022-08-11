<template>
  <b-form>
    <b-card>
      <b-form-group
        id="fieldset-1"
        label="Enter your name"
        label-for="input-1"
        valid-feedback="Thank you!"
      >
        <b-form-input id="input-1" v-model="name" trim></b-form-input>
        <b-button @click="checkInput">toantd</b-button>
      </b-form-group>
    </b-card>
    <b-link to="/123">Home page</b-link>
  </b-form>
</template>

<script lang="ts">
import {
  defineComponent,
  ref,
  useContext,
  useRoute,
  getCurrentInstance
} from '@nuxtjs/composition-api'
export default defineComponent({
  name: 'IndexPage',
  layout: 'app',
  setup() {
    const contextInstance = useContext()
    const route = useRoute()
    const currentInstance = getCurrentInstance()
    // const router = useRouter()
    const name = ref('')
    const checkInput = () => {
      debugger
      console.log(contextInstance)
      console.log(currentInstance)
    }
    return {
      route,
      name,
      checkInput,
      contextInstance,
    }
  },
})
</script>
