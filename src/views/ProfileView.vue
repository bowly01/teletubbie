<template>
 <div class="flex items-center justify-center space-x-5 h-screen">
    <div v-for="member in members" :key="member">
      <profile-card
        v-if="member.image"
        :name="member.name"
        :nickname="member.nickname"
        :birthday="member.birthday"
        :content="member.content"
        :image="member.image"
      ></profile-card>
    </div>
  </div>
</template>

<script>
import profileCard from "@/components/ProfileCard.vue";
export default {
  data() {
    return {
      members: [
        {
          name: "Puttipong",
          birthday: "24-01-2003",
          nickname: "boat",
          content: "KU81",
          image: "/assets/images/boat.jpg",
          isMember: true,
          score: 100
        },
        {
          name: "Putita",
          birthday: "03-08-2001",
          nickname: "bow",
          content: "KU81",
          image: "/assets/images/bow.jpg",
          isMember: true,
          score: 100
        },
        {
          name: "Hataichanok",
          birthday: "10-01-2003",
          nickname: "earth",
          content: "KU81",
          image: "/assets/images/earth.jpg",
          isMember: false,
          score: 51
        },
      ],
    };
  },
  components: {
    profileCard,
  },
};
</script>

<style></style>