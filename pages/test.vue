<template>
  <b-container class="container">
    <div>
      <h1 class="title">
        Project test
      </h1>
      <h2 class="subtitle">
        subtitles
      </h2>
      <div>
        <b-row>
          <b-col>
            <b-button variant="outline-primary">
              Poster une annonce
            </b-button>
          </b-col>
          <b-col>
            <b-button variant="outline-primary">
              Chercher une annonce
            </b-button>
          </b-col>
        </b-row>
      </div>
    </div>
  </b-container>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  layout: 'navbar'
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: calc(100vh - 56px);
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
</style>
