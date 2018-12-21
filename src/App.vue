<template>
  <div id="app">
    <h1>{{title}}</h1>
    <Navbar/>
    <AllFriends :friends="friends" @delete="deleteFriend"/>
    <OnlineFriends :friends="friends"/>
  </div>
</template>

<script>
import Navbar from "./Navbar";
import AllFriends from "./AllFriends";
import OnlineFriends from "./OnlineFriends";

export default {
  name: "app",
  components: {
    Navbar,
    AllFriends,
    OnlineFriends
  },
  data() {
    return {
      title: "My First View App",
      friends: [
        { name: "Mario", online: true },
        { name: "Peach", online: false },
        { name: "Toad", online: true },
        { name: "Bowser", online: false }
      ]
    };
  },
  methods: {
    deleteFriend(payload) {
      console.log(payload);
      this.friends = this.friends.filter(friend => {
        return friend.name !== payload.name;
      });
    }
  }
};
</script>

<style>
h1 {
  color: blue;
  text-align: center;
  font-weight: normal;
}
</style>