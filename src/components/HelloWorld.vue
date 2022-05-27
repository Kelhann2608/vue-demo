<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p v-if="abonnes == 0">Aucuns abonnés pour le moment 😥</p>
    <p v-else-if="abonnes == 1"> Une personne s'est abonnée, c'est un bon début ! 💪</p>
    <p v-else> {{ abonnes }} personnes se sont abonnées 🔥</p>
    <button v-on:click="subscribe()">S'abonner !</button>
    <div class="comment" v-for="(comment, index) in comments" v-bind:key="index">
      <h3>{{ comment.nom }}</h3>
      <p>{{ comment.commentaire}}</p>
      <div v-if="comment.note > 1">
        <span v-for="i in comment.note" v-bind:key="i">🍌</span>
        </div>
        <span v-else>💩</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function () {
    return {
      abonnes: 0,
      comments: [{
        nom: 'Jean François',
        commentaire: "c'est trop cool !",
        note: 4,
      },{
        nom: 'Amandine',
        commentaire: "J'adore ce que tu fais, continue !",
        note: 5,
      },{
        nom: 'Marc Aigri',
        commentaire: "c'est du caca !",
        note: 1,
      }
      ],
    }
  },
  methods: {
    subscribe: function () {
      this.abonnes++;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
p {
  font-size: 22px;
}
</style>
