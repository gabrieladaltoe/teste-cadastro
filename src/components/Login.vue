<template>

  <b-container class="bv-example-row">
      <b-row align-h="center" class="mt-5">
        <b-card class="text-center" >
          <b-form @submit.prevent="onSubmit" @reset.prevent="onReset" >
            <b-form-group
              id="input-group-1"
              label="Email:"
              label-for="input-1"
            >
              <b-form-input
                id="input-1"
                v-model="form.email"
                type="email"
                required
                placeholder="Seu email"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-2" label="Senha:" label-for="input-2">
              <b-form-input
                id="input-2"
                v-model="form.password"
                type="password"
                required
                placeholder="Sua senha"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-4">
              <b-form-checkbox-group v-model="form.checked" id="checkboxes-4">
                <b-form-checkbox value="me">Lembrar de mim</b-form-checkbox>
              </b-form-checkbox-group>
            </b-form-group>

            <b-button type="submit" variant="primary">Entrar</b-button>
          </b-form>
        </b-card>
      </b-row>
    </b-container>
</template>

<script>
    export default {
        data() {
            return {
            form: {
                    email: '',
                    password: '',
                    checked: false
                },       
            }
        },
        methods: {
            onSubmit() {
            alert(JSON.stringify(this.form))
            },
            onReset() {
            this.form.email = ''
            this.form.name = ''
            this.form.checked = []
            }
        }
    }

</script>

<style>
</style>
