<template>
  <div className="tweet">
  <ProfileImage/>

    <div className="body">
      <div className="top">
        
        <User :name="user.name" :handle="user.handle"/>
        <Timestamp :timestamp="timestamp" />
      </div>

          <p className="message">
        {{message}}
      </p>
      <div className="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>

import User from './tweet/User.vue';
import Timestamp from './tweet/Timestamp.vue';
import Message from './tweet/Message.vue';
import ProfileImage from './tweet/ProfileImage.vue';

export default {
components: {
  User,
  Timestamp,
  Message,
  ProfileImage,
  },

props: ["user", "timestamp", "message", "image"],
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
