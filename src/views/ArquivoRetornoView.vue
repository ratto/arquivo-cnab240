<template>
  <div class="retorno">
    <h1>Arquivo de Retorno</h1>
    <b-card no-body>
      <b-card-body>
        <FormRetorno />
      </b-card-body>
    </b-card>
  </div>
</template>

<script>
import FormRetorno from '@/components/FormRetorno.vue'

export default {
  components: {
    FormRetorno
  }
}
</script>

<style lang="sass" scoped>

</style>