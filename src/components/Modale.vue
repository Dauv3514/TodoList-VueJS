<template>
    <div class="bloc-modale" v-if="revele">
        <div class="overlay" v-on:click="toggleModale">
        </div>
        <div class="modale">
            <div v-on:click="toggleModale" class="btn-modale"> X
            </div>
            <div class="titre">
            <h2 id="title"> Comment utiliser le site ? </h2>
            <p> <br> - Ajouter votre tâche grâce au bouton AddTask <br> <br>
                - Supprimer une tâche grâce à la croix rouge </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Modale',
    props: ['revele', 'toggleModale']
}
</script>
<style scoped>

    .overlay {
        background: rgba(0,0,0,0.5);
        position: fixed;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
    }
    .modale {
        background: #f1f1f1;
        color: #333;
        height: 26%;
        width: 375px;
        position: fixed;
    }
    .btn-modale {
        position: absolute;
        top: 10px;
        right: 10px;
    }
    .titre {
        position: relative;
        top: 50px;
        left: 40px;
    }

    .titre h2 {
        color: red;
    }

    .titre p {
        top: 60px;
        color: black;
        font-size: 13px;
        font-weight: bold;
    }

</style>