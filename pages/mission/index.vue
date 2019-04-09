<template>
  <section class="missions">
    <Mission
      thumbnail="https://images.pexels.com/photos/73910/mars-mars-rover-space-travel-robot-73910.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260"
      title="New title here"
      previewText="best text here"
      :id="1"
    />
    <Mission
      v-for="mission in missions"
      :key="mission.id"
      :thumbnail="mission.thumbnail"
      :title="mission.title"
      :id="mission.id"
      :previewText="mission.previewText"
    />
  </section>
</template>

<script>
import Mission from "@/components/Mission";
export default {
  components: { Mission },
  asyncData() {
    //return axioxs call
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          missions: [
            {
              id: "2",
              previewText: "successful axios",
              title: "here is title from service call Tuesday",
              thumbnail:
                "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbFMono9uVXQnVWSbtUvrKLyIga16XXBZAo-iBGN_8OMwZRWlVRQ"
            },
            {
              id: "3",
              previewText: "successful axios",
              title: "here is title from service call Tuesday",
              thumbnail:
                "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbFMono9uVXQnVWSbtUvrKLyIga16XXBZAo-iBGN_8OMwZRWlVRQ"
            }
          ]
        });
      }, 1000);
    });
  }
};
</script>

<style scoped>
.missions {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-content: center;
}

.mission {
  box-sizing: border-box;
  width: auto;
  padding: 10px;
  border: 1px solid slategray;
  box-shadow: 4px;
  margin: 10px;
}

.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>
