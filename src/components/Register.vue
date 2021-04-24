<script>
  export default {
    data(){
      return {
        name : "",
        email : "",
        password : "",
        password_confirmation : "",
        is_admin : null
      }
    },

    methods: {
      register: function () {
        let data = {
          name: this.name,
          email: this.email,
          password: this.password,
          is_admin: this.is_admin
        }
        this.$store.dispatch('register', data)
       .then(() => this.$router.push('/'))
       .catch(err => console.log(err))
      }
    }
  }
</script>