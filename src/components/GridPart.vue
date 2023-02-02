<template>
        <div class="boxes">
            <div class="box">
                <div class="box-img">
                    <img src="./../assets/imgs/img1.jpg" alt="">
                </div>
                <div class="box-img-title">
                    <h6>img 1 photo</h6>
                </div>
                <div class="box-song-content pb-2">
                    <h4>Idiots</h4>
                    <p class="">The Best Songs is Sulatt</p>
                    <div class="img-btn">
                        <button class="btn btn-primary">Read More...</button>
                    </div>
                </div>
            </div>

            <div class="box">
                <div class="box-img">
                    <img src="./../assets/imgs/img2.jpg" alt="">
                </div>
                <div class="box-img-title">
                    <h6>img 1 photo</h6>
                </div>
                <div class="box-song-content pb-2">
                    <h4>Idiots</h4>
                    <p>The Best Songs is Sulatt</p>
                    <div class="img-btn">
                        <button class="btn btn-primary">Read More...</button>
                    </div>
                </div>
            </div>
            <div class="box">
                <div class="box-img">
                    <img src="./../assets/imgs/img3.jpg" alt="">
                </div>
                <div class="box-img-title">
                    <h6>img 1 photo</h6>
                </div>
                <div class="box-song-content pb-2">
                    <h4>Idiots</h4>
                    <p>The Best Songs is Sulatt</p>
                    <div class="img-btn">
                        <button class="btn btn-primary">Read More...</button>
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
                }
            ]
        }
    }

}
</script>

<style scoped>

.boxes{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));

}

.box{
    width: 250px;
    margin: 10px auto;
    border: 1px solid #ccc;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
    text-align: left;
}

.box .box-img{
    width: 248px;
}

.box .box-img-title h6{
    text-align: center;
}

.box .box-song-content p{
    padding-left: 20px;
}


.box .box-song-content .img-btn{
    margin-left: 20px;
}

.box .box-song-content h4{
    text-align: center;
}

.box .box-img img{
    width: 100%;
}


@media screen and (max-width: 992px) {

    .box{
        width: 230px;
    }

    .box .box-img{
        width: 230px;
        background: red;
    }

    .box img{
        width: 100%;
    }
}

@media screen and (max-width: 768px){
    .box{
        width: 200px;
    }

    .box .box-img{
        width: 200px;
    }

    .box .box-img img{
        widows: 100%;
    }
}

@media screen and (max-width: 576px) {
    .box{
        width: 180px;
    }

    .box .box-img{
        width: 178px;
    }

    .box .box-img img{
        width: 100%;
    }
}



</style>