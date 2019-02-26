<template>
  <b-container>
    <b-card
      img-src="https://picsum.photos/600/300/?image=25"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
    >
      <b-form v-if="show" @submit="onSubmit">
        <b-form-group
          id="exampleInputGroup1"
          class="labels"
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
          id="password"
          class="labels"
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

        <b-button type="submit" variant="light">
          Se connecter
        </b-button>
      </b-form>
      <div class="row mt-2">
        <nuxt-link to="/signup" class="col-6 link-undecorated">
          Je n'ai pas de compte
        </nuxt-link>
        <nuxt-link to="/forget" class="col-6 link-undecorated">
          J'ai oublié mon mot de passe
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
        food: null,
        checked: []
      },
      foods: [
        { text: 'Select One', value: null },
        'Carrots',
        'Beans',
        'Tomatoes',
        'Corn'
      ],
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
