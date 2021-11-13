<template>
    <div class="container my-5">
        <modale v-bind:revele="revele" v-bind:toggleModale="toggleModale"></modale>
        <Button v-on:click="toggleModale"
            :text="showAddTask ? 'Informations' : 'Informations'"
        />
    </div>
</template>
<script>
import Button from './Button.vue'
import Modale from './Modale'

export default {
    name: 'Contenu',
    data() {
        return {
            revele: false
        }
    },
    components: {
        Modale,
        Button
    },
    methods: {
        toggleModale(){
            this.revele = !this.revele
        }
    }
}

</script>