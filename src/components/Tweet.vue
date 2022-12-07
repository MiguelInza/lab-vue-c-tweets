<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />
    <div class="body">
      <div class="top">
        <User :tweet="tweet.user" />
        <Timestamp :tweet="tweet.timestamp" />
        <!--<span class="timestamp">{{tweet.timestamp}}</span>-->
      </div>

      <!--<p class="message"> {{tweet.message}} </p>-->
      <Message :tweet="tweet.message" />
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import Actions from './Actions.vue';
import Message from './Message.vue';
import ProfileImage from './ProfileImage.vue';
import Timestamp from './Timestamp.vue';
import User from './User.vue';

export default {
  components: {Actions, User, Message, ProfileImage, Timestamp},
  props: ["tweet"],
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
