<template>
  <b-container>
    <b-card
      header="Nom du projet"
      tag="article"
      style="width: 30rem;"
    >
      <b-form v-if="show" @submit="onSubmit">
        <b-form-group
          id="exampleInputGroup1"
          class="labels font-weight-bold"
          label="Adresse mail"
          label-for="exampleInput1"
        >
          <b-form-input
            id="exampleInput1"
            v-model="form.email"
            type="email"
            required
            placeholder="example@gmail.com"
          />
        </b-form-group>

        <b-form-group
          id="exampleInputGroup1"
          class="labels font-weight-bold"
          label="Prénom"
          label-for="exampleInput1"
        >
          <b-form-input
            id="exampleInput1"
            v-model="form.firstName"
            type="text"
            required
          />
        </b-form-group>

        <b-form-group
          id="exampleInputGroup1"
          class="labels font-weight-bold"
          label="Nom"
          label-for="exampleInput1"
        >
          <b-form-input
            id="exampleInput1"
            v-model="form.lastName"
            type="text"
            required
          />
        </b-form-group>

        <b-form-group
          id="password"
          class="labels font-weight-bold"
          label="Votre mot de passe"
          label-for="password"
        >
          <b-form-input
            id="password"
            v-model="form.password"
            type="password"
            required
            placeholder="Mot de passe"
          />
        </b-form-group>

        <b-form-group
          id="confirmPassword"
          class="labels font-weight-bold"
          label="Confirmez votre mot de passe"
          label-for="confirmPassword"
        >
          <b-form-input
            id="confirmPassword"
            v-model="form.confirmPassword"
            type="password"
            required
            placeholder="Mot de passe"
          />
        </b-form-group>


        <b-button type="submit" variant="light" class="fluid" block>
          S'inscrire
        </b-button>
      </b-form>
      <div class="row mt-2">
        <nuxt-link to="/login" class="col-12 link-undecorated">
          J'ai déjà un compte
        </nuxt-link>
      </div>
    </b-card>
  </b-container>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  layout: 'navbar',
  data() {
    return {
      form: {
        email: '',
        password: '',
        firstName: '',
        lastName: '',
        passwordConfirm: ''
      },
      show: true
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      alert(JSON.stringify(this.form))
    }
  }
}
</script>

<style>
.link-undecorated {
  text-decoration: none !important;
  color: #35495e;
}

.labels {
  color: #35495e;
  text-align: left;
  font-size: 14px;
}
</style>
