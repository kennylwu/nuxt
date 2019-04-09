<template>
  <section class="single-mission">
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


// <script>
// export default {
//   asyncData() {
//     //return axioxs call
//     return new Promise((resolve, reject) => {
//       setTimeout(() => {
//         resolve({
//           missions: [
//             {
//               id: "1",
//               descriptionText: "axios description",
//               title: "here is title from Monday",
//               thumbnail:
//                 "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbFMono9uVXQnVWSbtUvrKLyIga16XXBZAo-iBGN_8OMwZRWlVRQ"
//             }
//           ].find(el => el.id === context.params.id)
//         });
//       }, 1000);
//     });
//   }
// };
//
</script>
