<template>
  <div class="container w-full top-0">
    <div class="w-full items-center text-center align-center">
      <div class="py-8 text-6xl font-bold text-pink-500">
        Wildcard subdomains are here.
      </div>
      <iframe src="https://giphy.com/embed/AuwBPJztsEWkw" class="mx-auto" width="480" height="402" frameBorder="0" allowFullScreen></iframe>
      <div class="pt-8 font-semibold text-pink-500">
        {{ subdomain }}
      </div>
      <div class="pt-1 font-semibold text-pink-500">
        <a href="http://cleavr.io" class="text-blue-500 hover:text-blue-400">cleavr.io</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      subdomain: ""
    }
  },
  mounted() {
    const reg = new RegExp("www|sitename|test|localhost:3000");
    const parts = window.location.host.split(".");
    console.log(parts)
    this.subdomain = reg.test(parts[0]) ? parts[0] : "Add a subdomain 😜";
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
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

.links {
  padding-top: 15px;
}
</style>
