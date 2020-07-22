<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header" style="text-center">Tambah Buku</div>

                    <div class="card-body">
                        <form v-on:submit="submitPost()">
                          <div class="form-group">
                            <input type="text" v-model="posts.title" placeholder="Title" class="form-control">
                          </div>
                          <div class="form-group">
                            <textarea rows="5" type="text" v-model="posts.description" placeholder="Deskripsi" class="form-control"></textarea>
                          </div>
                          <div class="form-group">
                            <router-link to="/" class="btn btn-warning">Kembali</router-link>
                            <button class="btn btn-success">Simpan</button>
                          </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
  data:function() {
    return {
      posts: {
        title:'',
        description:'',
      },
      errors: []
    }
  },

 methods:{
  submitPost() {
    axios.post('/posts', this.posts)
    .then(response => {
      console.log(response)
      this.$router.push({path:'/'})
      this.posts = response.data
    })
    .catch(e => {
      this.errors.push(e)
    })

   }
  }
}
</script>
