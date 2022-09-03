<template>
  <div className="tweet">
    <ProfileImage :image="image"/>

    <div className="body">
      <div className="top">
        <User :handle="handle" :name="name" />
        <Timestamp :timestamp="timestamp" />
      </div>

      <Message :message="message" />
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
//import { defineComponent } from "@vue/composition-api";

export default {
 components: { ProfileImage, User, Timestamp, Actions, Message },
 props: ["name", "image", "handle", "message", "timestamp"]
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
