<template>
    
    <b-container>
       <h2 align-h="left">Cadastro</h2>
       <b-card class="text-center form-cadastro"  >
        <div>
          <b-form inline class="justify-content-center" >
            <label class="sr-only" for="inline-form-input-name">Name</label>
            <b-input
              id="inline-form-input-name"
              class="mb-2 mr-sm-2 mb-sm-0"
              placeholder="Jane Doe"
            ></b-input>

            <label class="sr-only" for="inline-form-input-username">Username</label>
            <b-input-group prepend="@" class="mb-2 mr-sm-2 mb-sm-0">
              <b-input id="inline-form-input-username" placeholder="Username"></b-input>
            </b-input-group>
            <b-button variant="primary">Save</b-button>
          </b-form>
        </div>

       </b-card>
       <div>
          <b-table striped hover :items="items" :fields="fields"></b-table>
       </div>
    </b-container>

</template>

<script>
    export default {
        data () {
            return {
                fields: ['Nome', 'email' ],
                items: [
                { Nome: 'Dickerson Macdonald', email: 'macdonald@email.com' },
                { Nome: 'Larsen Shaw', email: 'shaw@email.com' },
                { Nome: 'Geneva Wilson', email: 'wilson@email.com' },
                { Nome: 'Jami Carney', email: 'carney@email.com' }
                ]
            }
        }
    } 
</script>

<style>
</style>

