<template>
  <div class="gastos-por-veiculo">
    <h1>Lista de carros e seu gasto até aqui</h1>
    
     <li v-for="veiculo in veiculos">
      <p>Modelo: {{veiculo.nome}}</p>
      <p>Fabricante: {{veiculo.fabricante}}</p>
      <p>Placa: {{veiculo.placa}}</p>
      <p>Gasto: R${{veiculo.gasto}}</p>
    </li>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'GastosPorVeiculo',
  props: {
    veiculo: Object
  },
  
  mounted() {
    axios.get("http://localhost:8081/dashboard/gastos-por-veiculo").then(response => {
      this.veiculos = response.data
      console.log(this.veiculos)
    })
  },
  
  data() {
    return {
      veiculos: null
    }
  }
}
</script>
