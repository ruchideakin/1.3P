<template>
  <div class="container">
    <h1>Projects</h1>
    <p>Projects I participated in and/or developed.</p>

    <GitHubCard
      title="Formix"
      link="https://github.com/ruchideakin/task1.1p"
      :info="dowwwInfo"
      :loading="loading"
    >
      <p>
        Created an HTML page featuring essential HTML tags like image, table, and form, added CSS styling through inline, internal, and external styles. Additionally, initiated Git and GitHub, creating a repository to push code for version control and collaboration.
      </p>
    </GitHubCard>

    <GitHubCard
      title="Exploring Responsive Web Design and JavaScript Concepts"
      link="https://github.com/ruchideakin/1.2p-"
      :info="substatsInfo"
      :loading="loading"
    >
      <p>
        This task involved understanding and implementing responsive web design principles, emphasizing the importance of adaptability for various devices. It also included practicing JavaScript concepts, such as string, number, array, date, and function methods, within an HTML file to enhance interactivity and functionality.
      </p>
    </GitHubCard>

    <GitHubCard title="Portfolio" link="https://github.com/ruchideakin/1.3P" :info="bithesisInfo" :loading="loading">
      <p>
        Build a personal portfolio website showcasing my skills and projects using HTML, CSS, and Vue 3. Ensured responsiveness, implemented HTML elements, CSS styling with media queries, and Vue.js concepts like routing, user input handling, and components for a comprehensive presentation.
      </p>
    </GitHubCard>

  </div>
</template>

<script>
import GitHubCard from '@/components/GitHubCard.vue'

export default {
  components: {
    GitHubCard,
  },
  data() {
    return {
      loading: true,
      dowwwInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      substatsInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      bithesisInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      fatesInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      dotfilesInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
    }
  },
  mounted() {
    const githubApiUrl = 'https://api.github.com/repos'

    const dowwwAxios = this.axios.get(`${githubApiUrl}/spencerwooo/dowww`)
    const substatsAxios = this.axios.get(`${githubApiUrl}/spencerwooo/Substats`)
    const bithesisAxios = this.axios.get(`${githubApiUrl}/BITNP/BIThesis`)
    const fatesAxios = this.axios.get(`${githubApiUrl}/SecureCats/Evaluation_BackEnd`)
    const dotfilesAxios = this.axios.get(`${githubApiUrl}/spencerwooo/dotfiles`)

    this.axios
      .all([dowwwAxios, substatsAxios, bithesisAxios, fatesAxios, dotfilesAxios])
      .then(
        this.axios.spread((...resp) => {
          this.loading = false
          this.dowwwInfo = resp[0].data
          this.substatsInfo = resp[1].data
          this.bithesisInfo = resp[2].data
          this.fatesInfo = resp[3].data
          this.dotfilesInfo = resp[4].data
        }),
      )
      .catch(err => {
        this.loading = false
        // eslint-disable-next-line no-console
        console.error(err)
      })
  },
}
</script>

<style scoped>
.container .github-project-card:not(:last-child) {
  margin-bottom: 40px;
}
</style>
