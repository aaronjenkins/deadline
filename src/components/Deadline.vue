<template>
    <p>Here is your deadline: {{dateReturned}}</p>
</template>


<script>
import axios from "axios";

export default {
  data() {
    return {
      dateReturned: [],
      errors: []
    };
  },

  async created() {
    let url = `https://ubj33s2pl4.execute-api.us-east-2.amazonaws.com/default/randomdate`;
    let config = {
      headers: {
        "x-api-key": "cTKEhNDdht7LXyzr6xcUy6Sf3DBbFqeS2FH9bLMw"
      }
    };

    try {
      const response = await axios.get(url, config);
      this.dateReturned = new Date(response.data.body.replace(/['"]+/g, ''));
      this.dateReturned = this.dateReturned.toLocaleDateString('en-US', { weekday: 'long',  month: 'long', day: 'numeric' });
    } catch (e) {
      this.errors.push(e);
    }
  }
  
};
</script>