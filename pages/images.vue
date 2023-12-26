<template>
    <div class="images">
        <h2>This is an images page</h2>
        <FormComponent />
        <!--iterate through images object and display each image individually-->
        <div v-for="image in imageList">
            <!--actually use the image component-->
            <ImageComponent :src="image.src" :caption="image.caption" :title="image.title" />
        </div>
    </div>
</template>

<script>
// import the image component we created for use
import ImageComponent from '../components/ImageComponent.vue'
import FormComponent from '~/components/FormComponent.vue';

export default {
    name: "ImagesView",
    components: {
        ImageComponent,
        FormComponent
    },
    data: () => {
        return {
            imageList: [
                {
                    src: "travel.jpg",
                    caption: "Tooltipped image depicting air travel to various locations",
                    title: ''
                },
                {
                    src: "urban_vacation.jpg",
                    caption: "Tooltipped image of Paris near Eiffel Tower",
                    title: ''
                },
                {
                    src: "tropical_vacation.jpg",
                    caption: "Tooltipped image of a tropical island with pier",
                    title: ''
                }
            ],
        }
    },
    head: () => {
    return {
      title: "Travel Buddy Images",
      meta: [
        {
          charset: "utf-8"
        },
        {
          name: "viewport",
          content: "width=device-width, initial-scale=1"
        },
        {
          hid: "description",
          name: "description",
          content: "Helping you find pictures of your planned travels"
        }
      ]
    }
  },
}
</script>
  
<style scope>
@media (min-width: 1024px) {
    .about {
        min-height: 100vh;
        display: flex;
        align-items: center;
    }
}
</style>