<template>
  <div class="about">
    <h1>This is an about page</h1>
      <p v-for="val in resouce">{{val}}</p>
  </div>
</template>
<script>
    import axios from "axios";


    export default {
        name: 'home',
        created() {
            axios.get("/api/web/api/floors/v1?labe")
                .then((data) => {
                    console.log(data)
                    this.resouce = data.data.data.container.floor;
                })
        },
        components: {},
        data() {
            return {
                resouce: []
            }
        }
    }

</script>