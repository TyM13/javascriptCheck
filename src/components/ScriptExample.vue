<template>
  <div></div>
</template>

<script>
export default {

methods: {
    show_info: function() {
         for (let i = 0; i < this.tweets.length; i++) {
             document.body.insertAdjacentHTML(
        `afterbegin`,
        `<h1>Tweet:${this.tweets[i]}</h1>
        
         `
      )
         }
            if( this.logged_in === true) {
                document.body.insertAdjacentHTML(`afterbegin`, `<p>logged in:${this.logged_in}</p>
                <p>friends:${this.num_friends}</p>`)
                
            }else{
                document.body.insertAdjacentHTML(`afterbegin`, `<p>logged in:false</p>`)
            }

            
     
    
    
    }
},


  mounted() {
   this.show_info();
  },

  data() {
    return {
      tweets: [`i like pie`, `Ducks are the BEST`, `Cold Weather Please`],
      num_friends: 3,
      logged_in: true,
    };
  },

  name: "script-example",
};
</script>

<style scoped>
</style>