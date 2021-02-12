<template>
  <b-container>
    <div v-if="error">
      {{ error }}
    </div>
    <ul v-else>
      <hr />
      <b-container>
        <center>
        <h1>Shop Variety Of Products</h1>
        </center>
      </b-container>
      <hr />
      <b-row>
        <li v-for="proucts in proucts" :key="proucts.id">
          <b-col l="4">
            <b-card
              :title="proucts.title"
              :img-src="proucts.image.formats.thumbnail.url"
              img-alt="Image"
              img-top
              tag="article"
              style="max-width: 20rem"
              class="mb-2"
            >
              <b-card-text>
                {{ `${proucts.description}` }}
                <br>
                {{  }}
              </b-card-text>
            </b-card>
          </b-col>
        </li>
      </b-row>
    </ul>
  </b-container>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      proucts: [],
      error: null,
    };
  },
  async mounted() {
    try {
      const response = await axios.get(
        "https://shrouded-ridge-62535.herokuapp.com/proucts"
      );
      this.proucts = response.data;
    } catch (error) {
      this.error = error;
    }
  },
};
</script>

<style>
h1{
  margin: auto;
  left: 200px;
  right: auto;
  }
</style>