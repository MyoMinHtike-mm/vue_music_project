<template>
  <div class="container text-center align-items-center" id="twoCol">
    <div class="row">
        <div class="songCol col-md-6" >
            <h2 class="text-primary text-center">SongWriter</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium, molestias, reprehenderit aliquam iusto delectus numquam dolorum architecto eveniet tempore, quae adipisci enim suscipit deleniti ea velit ex! Quae, eius minus.</p>
            <button class="btn btn-primary">More Details...</button>
        </div>

        <div class="songCol col-md-6">
            <h2 class="text-primary text-center">SongSinger</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium, molestias, reprehenderit aliquam iusto delectus numquam dolorum architecto eveniet tempore, quae adipisci enim suscipit deleniti ea velit ex! Quae, eius minus.</p>
            <button class="btn btn-primary">More Details...</button>
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>


<style scoped>

#twoCol{
    position: relative;
    height: auto;
    margin: 3rem auto;
}
.container{
    width: 100%;
    height: 400px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
.row .songCol{
    width: 500px;
    text-align: left;
    padding: 20px;
    border: 1px solid #ccc;
    margin: 2rem;
    border-radius: 20px;    
}
.row .songCol h2{
    padding-bottom: 1rem;
}
.btn{
    text-align: center;
}




</style>