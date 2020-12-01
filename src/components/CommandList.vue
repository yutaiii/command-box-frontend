<template>
  <v-container>

    <v-row>
      <v-col cols="3" v-for="(item, i) in commandList" :key="i">
        <div class="command-box">
          <h2 class="box-title">{{ item.Title }}</h2>
          <v-row>
            <v-col cols="10">
              <span class="code">
                $ {{ item.Text }}
              </span>
            </v-col>
            <v-col cols="2">
              <v-icon @click="copyToClipboard(item.Text)">mdi-content-copy</v-icon>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>

  </v-container>
</template>

<script>
import axios from 'axios'

  export default {
    name: 'CommandList',

    data: () => ({
      commandList: [],
    }),

    mounted() {
      axios.get("http://localhost:8000/commands")
      .then(result => {
        this.commandList = result.data;
      })
      .catch(e => {
        console.log(e, "error")
      })
    },

    methods: {
      copyToClipboard(text) {
        navigator.clipboard.writeText(text)
        .then(() => {
          alert('copied to clipboard!');
        })
        .catch(e => {
          alert('Error:' + e);
        })
      }
    }
  }
</script>

<style scoped>
.command-box {
  background-color: #f0f0f0;
  padding: 10px;
}

.box-title {
  font-weight: bold;
  word-wrap: break-word;
  text-align: left;
}

.code {
  color: #f0f0f0;
  background-color: black;
  padding: 5px;
  float: left;
  text-align: left;
  word-break: break-all ;
}

.test {
  background-color: aqua;
}
</style>
