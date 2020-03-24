<template>
  <div>
    <h1>{{ msg }}</h1>

    <p
      style="margin-top: 1rem"
    >Test this page in production environment (Docker). If you can see my Github Page below, that means the Nginx proxy works :)</p>

    <p>Don't forget to give my repo a star if you find this helpful :)</p>

    <div v-html="myGithubPage" style="margin-top: 5rem"></div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "HelloWorld",

  props: {
    msg: String
  },

  data() {
    return {
      myGithubPage: null
    };
  },

  created() {
    axios.get("/zhzhang-4390").then(res => (this.myGithubPage = res.data));
  }
};
</script>
