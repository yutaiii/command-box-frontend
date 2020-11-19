<template>
  <v-container>

    <v-row class="text-center">
      <v-col cols="3">
        <div class="command-box">
          <h2 class="box-title">安全にforce pushする</h2>
          <v-row>
            <v-col cols="10">
              <span class="code">
                $ git push --force-with-lease [remote-name] [branch-name]
              </span>
            </v-col>
            <v-col cols="2">
              <v-icon>mdi-content-copy</v-icon>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="3">
        <div class="command-box">
          <h2 class="box-title">安全にforce pushする</h2>
          <v-row>
            <v-col cols="10">
              <span class="code">
                $ git push --force-with-lease [remote-name] [branch-name]
              </span>
            </v-col>
            <v-col cols="2">
              <v-icon>mdi-content-copy</v-icon>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="3">
        <div class="command-box">
          <h2 class="box-title">安全にforce pushする</h2>
          <v-row>
            <v-col cols="10">
              <span class="code">
                $ git push --force-with-lease [remote-name] [branch-name]
              </span>
            </v-col>
            <v-col cols="2">
              <v-icon>mdi-content-copy</v-icon>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="3">
        <div class="command-box">
          <h2 class="box-title">安全にforce pushする</h2>
          <v-row>
            <v-col cols="10">
              <span class="code">
                $ git push --force-with-lease [remote-name] [branch-name]
              </span>
            </v-col>
            <v-col cols="2">
              <v-icon>mdi-content-copy</v-icon>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>

  </v-container>
</template>

<script>
  export default {
    name: 'CommandList',

    data: () => ({
    }),
  }
</script>

<style scoped>
.command-box {
  background-color: #f0f0f0;
  padding: 10px;
}

.box-title {
  font-weight: bold;
}

.code {
  color: #f0f0f0;
  background-color: black;
  padding: 5px;
  float: left;
}

.test {
  background-color: aqua;
}
</style>
