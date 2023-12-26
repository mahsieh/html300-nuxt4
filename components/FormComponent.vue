<template>
    <div class="form-container">
        <div class="form-group">
            <label for="loc">Where would you like to go?</label><br>
            <input type="text" id="loc" class="form-control" name="country" placeholder="Type a country">
            <small id="locHelp" class="form-text text-muted">Please use three letter country codes</small>
        </div>
        <div class="form-group">
            <label for="when">When do you want to travel?</label>
            <input type="month" id="when" class="form-control" name="travelMonth">
        </div>
    </div>
</template>

<script>


export default {
    // create the Form component
    name: "FormComponent",
    // define 3 props for the Form Component
    props: {
        src: {
            type: String,
            required: true,
            /*use a validation against image source to verify file type*/
            validator: function (value) {
                const validFormats = /\.(jpg|png|jpeg)$/i
                return validFormats.test(value)
            }
        },
        caption: {
            type: String,
            required: true,
        },
        title: {
            type: String,
            default: 'Travel Vibes'
        }
    }
}
</script>

<style>
/*set styling for the visible border */
.image-border {
    border: 1rem solid purple;
}
</style>