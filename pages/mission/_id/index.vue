<template>
  <section class="single-mission">
    <h1>Page: {{$route.params.id}}</h1>
    <h1>{{ missions.title }}</h1>
    <div :id="missions.id">
      <img :src="missions.thumbnail" alt="space">
    </div>

    <p>{{ missions.descriptionText}}</p>
  </section>
</template>

<style scoped>
.single-mission {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 20px;
}
</style>

<script>
export default {
  asyncData(context) {
    //return axioxs call
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          missions: [
            {
              id: "1",
              descriptionText: "successful routing",
              title: "here is title from service call Tuesday",
              thumbnail:
                "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbFMono9uVXQnVWSbtUvrKLyIga16XXBZAo-iBGN_8OMwZRWlVRQ"
            },
            {
              id: "2",
              descriptionText: "successful routing",
              title: "here is title from service call Tuesday",
              thumbnail:
                "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbFMono9uVXQnVWSbtUvrKLyIga16XXBZAo-iBGN_8OMwZRWlVRQ"
            },
            {
              id: "3",
              descriptionText: "successful routing",
              title: "here is title from service call Tuesday",
              thumbnail:
                "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbFMono9uVXQnVWSbtUvrKLyIga16XXBZAo-iBGN_8OMwZRWlVRQ"
            }
          ].find(el => el.id === context.params.id)
        });
      }, 1000);
    });
  }
};
</script>

