<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark" sticky>
      <b-navbar-brand nuxt-link to="/">
        NavBar
      </b-navbar-brand>

      <b-navbar-toggle target="nav_collapse" />

      <b-collapse id="nav_collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item nuxt-link to="/">
            S'inscrire
          </b-nav-item>
          <b-nav-item nuxt-link to="/login">
            Se connecter
          </b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Search" />
            <b-button size="sm" class="my-2 my-sm-0" type="submit">
              Search
            </b-button>
          </b-nav-form>

          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item to="#">
              EN
            </b-dropdown-item>
            <b-dropdown-item to="#">
              FR
            </b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown right>
            <!-- Using button-content slot -->
            <template slot="button-content">
              <em>
                User
              </em>
            </template>
            <b-dropdown-item>
              <nuxt-link to="/login">
                Sign In
              </nuxt-link>
            </b-dropdown-item>
            <b-dropdown-item>
              <nuxt-link to="/Signup">
                Signout
              </nuxt-link>
            </b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <nuxt />
  </div>
</template>

<style>
.container {
  margin: 0 auto;
  min-height: calc(100vh - 57px) !important;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
