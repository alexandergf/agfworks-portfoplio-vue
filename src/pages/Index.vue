<template>
  <Layout>

    <section>
      <v-container>
        <v-row>
          <v-col sm="6">
            <g-image alt="Profile image" src="~/profile.jpg" width="400" />
          </v-col>
          <v-col sm="6">
            <h1>Hi, I'm Alexander</h1>
            <p>I'm a web developer...</p>
          </v-col>
        </v-row>
      </v-container>
      
    </section>

  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
