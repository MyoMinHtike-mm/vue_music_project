<template>
    <div class="container mb-5 d-flex justify-content-around align-items-center" id="songGridView">
        <div v-for="imgBox in imgBoxes" :key="imgBox.id" class="" id="imgBoxes">     
            <div class="img-box">
                <h6 class="text-center">
                    <img :src="require(`./../assets/imgs/${imgBox.img}`)" alt=""/>
                    <div class="pt-2">{{ imgBox.imgPhoto }}</div>
                </h6>
                <div class="img-content p-3">
                    <h5>{{ imgBox.songTitle }}</h5>
                    <p>{{ imgBox.songContent }}</p>
                    <button class="btn btn-primary">ReadMore</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

    data(){
        return{
            imgBoxes :[
                {   
                    img: 'img1.jpg',
                    imgPhoto : 'Img1 Photo',
                    songTitle: 'Idiots',
                    songContent: 'The Best Songs is Sulatt',
                },
                {
                    img: 'img2.jpg',
                    imgPhoto : 'Img2 Photo',
                    songTitle: 'Big Bag',
                    songContent: 'The Best Songs is Villan',
                },
                {
                    img: 'img3.jpg',
                    imgPhoto : 'Img3 Photo',
                    songTitle: 'Fokker',
                    songContent: 'The Best Songs is ZatPot',
                },
            ]
        }
    }

}
</script>




<style scoped>



#songGridView{
    padding: 2rem;
}

#imgBoxes{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(10rem, 1fr));
    place-items: center;
}
#imgBoxes .img-box img{
    width: 200px;
}
.img-box{
    height: auto;
    border: 1px solid #ccc;
    border-radius: 10px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}





@media screen and (max-width: 992px) {
    #imgBoxes{
            grid-template-columns: repeat(auto-fit, minmax(10rem, 1fr));
    }
    .img-box{
        display: block;
    }
}

@media screen and (max-width: 768px) {
    #imgBoxes{
        display: grid;
        grid-template-columns: 1fr 1fr;
    }
    #imgBoxes .img-box img{
        width: 150px;
    }
}



</style>