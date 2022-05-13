<template>
  <div class="p-5">
    <div class="flex flex-col gap-y-2">
      <label for="url">Name</label>
      <input
        v-model="url"
        type="url"
        name="url"
        class="w-100 px-4 py-2 border border-gray-300 outline-none focus:border-gray-400"
      />
    </div>
    <button
      @click="fetchResults"
      class="px-6 py-2 text-sm rounded shadow bg-slate-100 hover:bg-slate-200 text-slate-500"
    >
      Button
    </button>

    <!-- <p v-if="$fetchState.pending">Fetching issues...</p>
    <p v-else-if="$fetchState.error">An error occurred :(</p> -->
    <div>
      <h1>a11y issues</h1>
      <ul>
        <li v-for="(issue, i) in results.issues" :key="i">
          {{ issue.message }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
// TODO: get / set url parameter so users can link to it
export default {
  name: 'IndexPage',
  data: () => ({
    results: [],
    url: 'https://matthias-andrasch.eu',
  }),
  methods: {
    async fetchResults() {
      // TODO: how to get the correct url for server?!
      // https://axios.nuxtjs.org/usage/
      const results = await this.$axios.$post(
        //'/pa11y-api/',
        'http://localhost:3000/pa11y-api/',
        {
          url: this.url,
        },
        { progress: true }
      )
      console.log('results from axios', results)
      this.results = results
    },
  },
  /*async fetch() {
    // TODO: how to get the correct url for server?!
    // https://axios.nuxtjs.org/usage/
    const results = await this.$axios.$post(
      //'/pa11y-api/',
      'http://localhost:3000/pa11y-api/',
      {
        url: 'https://matthias-andrasch.eu',
      }
    )
    console.log('results from axios', results)
    this.results = results
  },*/
}
</script>
