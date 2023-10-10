<template>
    <v-row>
      <v-col cols="3" sm="3" v-for="(popular, i) in populars" :key="i">
        <v-card class="mx-auto my-12 pb-4" max-width="374">
          <v-img height="250" class="mx-4" :src="popular.img"></v-img>
  
          <v-card-item class="mt-n4">
            <v-card-title class="text-center">{{ popular.title }}</v-card-title>
          </v-card-item>
  
          <v-card-text>
            <div class="text-center">
              {{ popular.bio }}
            </div>
            <v-row align="center" class="mx-0 mt-2">
              <v-rating
                :model-value="4.5"
                color="amber"
                density="compact"
                half-increments
                readonly
                size="small"
              ></v-rating>
              <v-spacer></v-spacer>
              <div class="text-grey ms-4">{{ popular.price }}</div>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </template>
  
  <script>
  export default {
    data: () => ({
      populars: [
        {
          img: "image/1.png",
          title: "Go-Pro",
          price: "$ 123.456",
          bio: " Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque eget dapibus leo. Sed quis malesuada nisl. Proin mattis ligula eu ipsum vestibulum, eget facilisis sem ultrices. Suspendisse accumsan, lacus non ultricies gravida, ex turpis volutpat velit, ut dignissim est ex eu nunc. In hac habitasse platea dictumst. Aenean at neque dolor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec nec tellus a neque vulputate feugiat. Ut maximus tellus sed metus pulvinar, a dictum ipsum ultrices. Duis id sagittis dolor. Ut turpis mauris, rutrum ut mattis eu, consectetur in diam. Interdum et malesuada fames ac ante ipsum primis in faucibus.",
        },
        {
          img: "image/2.png",
          title: "Earphone",
          price: "$ 2.345",
          bio: " Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque eget dapibus leo. Sed quis malesuada nisl. Proin mattis ligula eu ipsum vestibulum, eget facilisis sem ultrices. Suspendisse accumsan, lacus non ultricies gravida, ex turpis volutpat velit, ut dignissim est ex eu nunc. In hac habitasse platea dictumst. Aenean at neque dolor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec nec tellus a neque vulputate feugiat. Ut maximus tellus sed metus pulvinar, a dictum ipsum ultrices. Duis id sagittis dolor. Ut turpis mauris, rutrum ut mattis eu, consectetur in diam. Interdum et malesuada fames ac ante ipsum primis in faucibus.",
        },
        {
          img: "image/3.png",
          title: "H/K Speaker",
          price: "$ 52.345",
          bio: " Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque eget dapibus leo. Sed quis malesuada nisl. Proin mattis ligula eu ipsum vestibulum, eget facilisis sem ultrices. Suspendisse accumsan, lacus non ultricies gravida, ex turpis volutpat velit, ut dignissim est ex eu nunc. In hac habitasse platea dictumst. Aenean at neque dolor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec nec tellus a neque vulputate feugiat. Ut maximus tellus sed metus pulvinar, a dictum ipsum ultrices. Duis id sagittis dolor. Ut turpis mauris, rutrum ut mattis eu, consectetur in diam. Interdum et malesuada fames ac ante ipsum primis in faucibus.",
        },
        {
          img: "image/4.png",
          title: "Apple Watch",
          price: "$ 699",
          bio: " Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque eget dapibus leo. Sed quis malesuada nisl. Proin mattis ligula eu ipsum vestibulum, eget facilisis sem ultrices. Suspendisse accumsan, lacus non ultricies gravida, ex turpis volutpat velit, ut dignissim est ex eu nunc. In hac habitasse platea dictumst. Aenean at neque dolor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec nec tellus a neque vulputate feugiat. Ut maximus tellus sed metus pulvinar, a dictum ipsum ultrices. Duis id sagittis dolor. Ut turpis mauris, rutrum ut mattis eu, consectetur in diam. Interdum et malesuada fames ac ante ipsum primis in faucibus.",
        },
      ],
    }),
  };
  </script>
  
  <style></style>
  