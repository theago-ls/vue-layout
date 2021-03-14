<template>
  <section class="card">
    <p class='title'>Pronto para planejar seu sossego?</p>
    <p class='subtitle'>Agende uma consultoria sem compromisso pelo formulário abaixo!</p>
    <Input id='name' label='Nome:' ></Input>
    <Input id='email' label='E-mail:' ></Input>
    <Input id='maritalStatus' label='Estado civil:' ></Input>
    <Input id='profession' label='Profissão:' ></Input>
    <Input id='phone' label='Telefone/WhatsApp:' ></Input>
    <Input id='monthlyIncome' label='Renda mensal:' ></Input>
    <Button label='Enviar'></Button>
  </section>
</template>

<script lang="ts">
import Vue from 'vue';
import Input from './Input.vue';
import Button from './Button.vue';

export default Vue.extend({
  name: 'FormCard',
  components: {
    Input,
    Button,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.card {
  margin-left: 12%;
  display: flex;
  flex-direction: column;
  width: 30%;
  height: 60%;
  background: #313072;
  padding: 25px 35px;
  text-align: left;
  transform: translateY(50%);

  .title {
    font-size: 38px;
    font-weight: bold;
    color: #ff9b23;
    line-height: 1.2;
  }

  .subtitle {
    font-size: 28px;
    margin: 20px 0;
    color: rgba(255,255,255,0.8);
  }

  button {
    margin-top: 30px;
  }
}

@media screen and (max-width: 968px) {
  .card {
    width: 84%;
    margin-left: 0;
    transform: translateY(10%);
  }
}

@media screen and (max-width: 728px) {
  .card {
    width: 75%;
  }
}
</style>
