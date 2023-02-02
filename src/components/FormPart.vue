<template>
    <div class="container d-flex justify-content-between mt-5" id="mainFav">
        <div id="favSong-lists">
            <h2 class="text-center pb-2 text-secondary">The Favourite Songs</h2>
            <ul class="list-group">
                <li class="list-group-item" aria-current="true">
                    <i class="fa fa-address-book-o me-3" aria-hidden="true"></i>
                    The Best Seller Album
                </li>
                <li class="list-group-item">
                    <i class="fa fa-star-o me-3" aria-hidden="true"></i>
                    The Best Seller Rating
                </li>
                <li class="list-group-item">
                    <i class="fa fa-user me-3" aria-hidden="true"></i>
                    The Best Seller Singer
                </li>
                <li class="list-group-item">
                    <i class="fa fa-shopping-cart me-3" aria-hidden="true"></i>
                    The Best Seller Shop
                </li>
                <li class="list-group-item">
                    <i class="fa fa-podcast me-3" aria-hidden="true"></i>
                    The Best Seller Channel
                </li>
            </ul>
        </div>
    <div>

    <form @submit.prevent="submit">
        <label for="newSinger">SongWriter</label>
        <input type="text"  class="form-control" v-model="newSinger" placeholder="Enter your music writer" required>
        <small v-if="errEmail" class="errEmail">{{ errEmail }}</small>
        <label for="newTitle">SongTitle</label>
            <input type="text" class="form-control" v-model="newTitle" placeholder="Enter your music title" required>
        <small v-if="errMsg" class="errPasswordMsg">{{ errMsg }}</small>

        <label for="role">Music Role</label>
        <select v-model="role" value="Choose Position" required>
            <option value="rock">Rock Music</option>
            <option value="metal">Metal Music</option>
            <option value="rap">Rap Music</option>
            <option value="r&b">R&B Music</option>
            <option value="pop">Pop Music</option>
        </select>
        <input type="submit" value="Add New Music" class="btn btn-primary text-light w-100 mt-3" @click="showModal=true">
    </form>
    
        </div>
    </div>


    <div class="songSection container">
        <h2 class="text-secondary">Popular' Song</h2>
        <div class="d-flex mb-3 input-group">
            <input type="text" class="form-control" v-model="newList">
            <button class="btn btn-primary">Search</button>
        </div>    
        <div class="songs">
            <div v-for="song in filterMusic" class="song" :key="song.id">
                <span class="cross float-end" @click="deleteItem(song)">&#10006;</span>
                <h4>{{ song.singer }}</h4>
                <p> Music Title - {{  song.title }}</p>
                <p> Music Type - {{ song.role }}</p>
                <div class="text-center">
                    <button class="btn btn-primary">More...</button>
                </div>
                <div>
            </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

    data(){
        return{
            newSinger: '',
            newTitle: '',
            email: "",
            password: "",
            errMsg: "",
            errEmail: "",
            role: [],
            newList: "",
            showModal: false,

            songs: [
                {
                    singer: 'Raymond',
                    title: 'Su Latt',
                    role: 'metal'
                },
                {
                    singer: 'Han Htoo Lwin',
                    title: 'Villain',
                    role: 'rock'
                },
                {
                    singer: 'Fokker',
                    title: 'metal',
                    role: 'rock'

                },
                {
                    singer: 'Kaung Kaung',
                    title: 'Pyaw Nay Par',
                    role: 'r&b'
                },
                {
                    singer: 'GLatt',
                    title: 'Bal Si mhar Lal',
                    role: 'rock'
                },
                {
                    singer: 'Wai La',
                    title: 'a mite ma',
                    role: 'rap'
                },

                {
                    singer: 'Wa Na',
                    title: 'ma',
                    role: 'rock'
                }
            ]
        }
    },

    methods : {
        addNewSong(){
            console.log(this.newSinger, this.newSong);
        },

        submit(){  
            this.songs.push({
                singer: this.newSinger,
                title: this.newTitle,
                role: this.role
            });

            this.newSinger = "";
            this.newTitle = "";
            this.role = ""

            this.$emit('close');
        },

        deleteItem(song){
            this.songs = this.songs.filter((loopSong)=>{
                return loopSong.singer !== song.singer;
            })
        }
    },

    computed: {
        filterMusic(){
            return this.songs.filter((filterSong)=>{
                return filterSong.singer.toLowerCase().includes(this.newList.toLowerCase())
            })
        }
    }

}
</script>


<style scoped>


form{
    width: 600px;
    background: #fff;
    padding: 40px;
    text-align: left;
    border-radius: 20px;
    margin: 30px auto;
}

label{
    color: #aaa999;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}

input, select{
    width: 100%;
    display: block;
    padding: 10px 6px;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #aaa;
    color: #555;
}

input[submit]{
    background: lightblue;
}


input[placeholder]{
    font-size: 0.8rem;
    color: #555;

}

input[type="checkbox"]{
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 2px;
}

#favSong-lists{
    width: 400px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

#favSong-lists h2{
   border-bottom: 2px solid #ccc;
   margin-bottom: 1.5rem;
}

#favSong-lists ul li{
    line-height: 4rem;
    font-size: 1.1rem;
    color: #aaa;
}

#favSong-lists ul li:hover{
    color: #555;
    cursor: pointer;
}


#favSong-lists ul li i{
    font-size: 1.5rem;
}

.errPasswordMsg, .errEmail{
    display: block;
    padding-top: 10px;
    color: crimson;
}

.songSection{
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

.songSection h2{
    text-align: center;
    padding-bottom: 2rem;
    font-family: Arial, Helvetica, sans-serif;
}

.songs{
    display: grid;
    gap: 2rem;
    grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
    place-items: center;
}
.songs .song{
    width: 250px;
    border: 1px solid #ccc;
    padding: 1rem;
    border-radius: 20px;
} 
.songs .song h4{
    color: red;
    text-align: center;
}
.songs .song p{
    font-size: 1.1rem;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
.cross{
    cursor: pointer;
}

@media screen and (max-width: 992px) {
    #mainFav{
        flex-direction: column;
    }    
}

@media screen and (max-width: 768px) {

    #favSong-lists{
        width: 100%;
    }

    form{
        width: 100%;
    }
}


</style>