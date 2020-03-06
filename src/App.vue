<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import { CometChat } from "@cometchat-pro/chat";
import "./App.css";
export default {
  data() {
    return {};
  },
  created() {
    this.initializeApp();
  },
  methods: {
    initializeApp() {
      var appID = '379556fe47c979';
      CometChat.init(appID).then(
        () => {
          console.log("Initialization completed successfully");
        },
        error => {
          console.log("Initialization failed with error:", error);
        }
      );
    }
  }
};
</script>