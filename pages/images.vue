<template>
    <div class="images">
        <h1>This is an images page</h1>
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
    }
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