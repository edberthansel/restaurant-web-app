<template>
  <div>
    <b-navbar toggleable="lg">
      <b-icon icon="border-width"></b-icon>

      <b-navbar-brand href="#" class="navbar-brand-custom">Chukwudi</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-input-group size="sm" class="mb-2 input-search-custom">
            <b-input-group-prepend is-text>
              <b-icon icon="search"></b-icon>
            </b-input-group-prepend>
            <b-form-input
              type="search"
              placeholder="Search"
            ></b-form-input>
          </b-input-group>
        </b-navbar-nav>

        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown right>
            <template v-slot:button-content>
              <b-icon icon="person" aria-hidden="true"></b-icon>
            </template>
            <b-dropdown-item href="#">Login</b-dropdown-item>
            <b-dropdown-item href="#">Register</b-dropdown-item>
          </b-nav-item-dropdown>

          <button class="btn btn-header-number" type="button">3</button>
            
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>

export default {
  name: "Header",
  components: {
    
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
