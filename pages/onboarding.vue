<template>
  <div class="container register-page">
    <div class="row">
      <div class="col-md-5 ml-auto">
        <div class="info-area info-horizontal mt-5">
          <div class="icon icon-warning">
            <i class="tim-icons icon-pencil"></i>
          </div>
          <div class="description">
            <h3 class="info-title">1. Dai un nome al progetto</h3>
          </div>
        </div>
        <div class="info-area info-horizontal">
          <div class="icon icon-primary">
            <i class="tim-icons icon-email-85"></i>
          </div>
          <div class="description">
            <h3 class="info-title">2. Scansiona la tua email</h3>
          </div>
        </div>
        <div class="info-area info-horizontal">
          <div class="icon icon-info">
            <i class="tim-icons icon-atom"></i>
          </div>
          <div class="description">
            <h3 class="info-title">3. Invita il tuo team</h3>
          </div>
        </div>
      </div>

      <div class="col-md-7 mr-auto">
        <p>Fai finta di aver fatto tutto questo</p>
        <base-button type="primary" round block size="lg" @click="$router.push('/projects/e-Virdis')">
          Vai avanti
        </base-button>
      </div>
    </div>
  </div>
</template>
<script>
import { BaseCheckbox } from '@/components';

export default {
  name: 'register-page',
  layout: 'auth',
  components: {
    BaseCheckbox
  },
  data() {
    return {
      model: {
        email: 'alessandro.macagno@ememory.it',
        fullName: 'Alessandro Macagno',
        password: 'changeme'
      }
    };
  },
  methods: {
    getError(fieldName) {
      return this.errors.first(fieldName);
    },
    async register() {
      let isValidForm = await this.$validator.validateAll();
      if (isValidForm) {
        // TIP use this.model to send it to api and perform register call
        this.$router.push('/projects/e-Virdis')
      }
    }
  }
};
</script>
<style></style>
