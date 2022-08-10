<template>
  <div class="dashboard">
    <GastosPorVeiculo></GastosPorVeiculo>
  </div>
</template>

<script>
// @ is an alias to /src
import GastosPorVeiculo from '@/components/GastosPorVeiculo.vue';


export default {
  name: 'Dashboard',
  components: {
    GastosPorVeiculo
  }
}
</script>
