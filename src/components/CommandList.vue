<template>
  <v-container>

    <v-row class="text-center">
      <v-col cols="3" v-for="(item, i) in commandList" :key="i">
        <div class="command-box">
          <h2 class="box-title">{{ item.title }}</h2>
          <v-row>
            <v-col cols="10">
              <span class="code">
                $ {{ item.text }}
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
      commandList: [
        {
          title: '安全にforce pushする',
          text: 'git push --force-with-lease [remote-name] [branch-name]',
        },
        {
          title: '安全にforce pushする',
          text: 'git push --force-with-lease [remote-name] [branch-name]',
        },
        {
          title: '安全にforce pushする',
          text: 'git push --force-with-lease [remote-name] [branch-name]',
        },
        {
          title: '安全にforce pushする',
          text: 'git push --force-with-lease [remote-name] [branch-name]',
        }
      ],
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
