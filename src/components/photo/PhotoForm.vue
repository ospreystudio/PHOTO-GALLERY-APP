<template>
    <v-container>
        <v-row class="d-flex"> 
            <v-text-field v-model="title"  placeholder="Enter the name of photo"/>
            <v-file-input v-model="img" placeholder="Select a photo"/>
            <v-btn @click="addPhoto" color="cyan" class="mx-2">Add Photo</v-btn>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            title: '',
            img: []
        }
    },
    methods: {
        addPhoto() {
        const reader = new FileReader()
        reader.onload = () => {
            let photo = {
                id: Date.now(),
                title: this.title,
                url: reader.result
        }
         this.$emit('addPhoto', photo)
    }
      reader.readAsDataURL(this.img)    
    }

    }
}

</script>
