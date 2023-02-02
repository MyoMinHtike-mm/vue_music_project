<template>
  <footer>
        <h2 class="text-secondary">Favourite Popular Channel Links</h2>
        <div class="footer-links container">
            <div class="footer-link">
                <h4>Popular Channel</h4>
                <ul class="popularSong-links">
                    <li><i class="fa fa-home me-2" aria-hidden="true"></i>Home</li>
                    <li><i class="fa fa-television me-2" aria-hidden="true"></i>Channel</li>
                    <li><i class="fa fa-steam me-2" aria-hidden="true"></i>Streaming</li>
                    <li><i class="fa fa-archive me-2" aria-hidden="true"></i>Packages</li>
                    <li><i class="fa fa-phone me-2" aria-hidden="true"></i>Contact</li>
                </ul>
            </div>
            <div class="footer-link">
                <h4>Favourite Channel</h4>
                <ul class="favSong-links">
                    <li><i class="fa fa-home me-2" aria-hidden="true"></i>Home</li>
                    <li><i class="fa fa-television me-2" aria-hidden="true"></i>Channel</li>
                    <li><i class="fa fa-steam me-2" aria-hidden="true"></i>Streaming</li>
                    <li><i class="fa fa-archive me-2" aria-hidden="true"></i>Packages</li>
                    <li><i class="fa fa-phone me-2" aria-hidden="true"></i>Contact</li>
                </ul>
            </div>
            <div class="footer-link">
                <h4>Streaming Channel</h4>
                <ul class="bestSellerSong-links">
                    <li><i class="fa fa-home me-2" aria-hidden="true"></i>Home</li>
                    <li><i class="fa fa-television me-2" aria-hidden="true"></i>Channel</li>
                    <li><i class="fa fa-steam me-2" aria-hidden="true"></i>Streaming</li>
                    <li><i class="fa fa-archive me-2" aria-hidden="true"></i>Packages</li>
                    <li><i class="fa fa-phone me-2" aria-hidden="true"></i>Contact</li>
                </ul>
            </div>
            <div class="footer-link">
                <h4>News Channel</h4>
                <ul class="latestSong-links">
                    <li><i class="fa fa-home me-2" aria-hidden="true"></i>Home</li>
                    <li><i class="fa fa-television me-2" aria-hidden="true"></i>Channel</li>
                    <li><i class="fa fa-steam me-2" aria-hidden="true"></i>Streaming</li>
                    <li><i class="fa fa-archive me-2" aria-hidden="true"></i>Packages</li>
                    <li><i class="fa fa-phone me-2" aria-hidden="true"></i>Contact</li>
                </ul>
            </div>
        </div>
        <p class="text-secondary">2022 @copyright by Asnarsar</p>
  </footer>
</template>

<script>
export default {

}
</script>

<style scoped> 

body{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

footer{
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;

}

footer h2{
    text-align: center;
}

footer .footer-links{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
    gap: 1rem;
    margin-top: 3rem;
  
    /* grid-template-items: repeat(minmax(420px), 1fr); */
}

footer .footer-links .footer-link{
    /* background: rgba(0, green, blue, alpha); */
    border: 1px solid #ccc;
    box-shadow: 2px solid rgba(0, 0, 0, 0.3);
    /* padding-top: 2rem;
    padding-bottom: 2rem; */
    padding: 0.5rem 0rem;
}

footer .footer-links .footer-link h4{
    text-align: center;
    color: rgba(0, 0, 0, 0.7)
}

footer .footer-links .footer-link ul{
    margin-top: 1.5rem;
}

footer .footer-links .footer-link li{
    /* line-height: 2.3rem;
    font-size: 1.1rem;
    list-style: none; */
    line-height: 2rem;
    list-style: none;
    cursor: pointer;
    color: rgba(0, 0, 0, 0.4);
    /* background: red; */
    text-align: left;
    margin-left: -1rem;
    font-size: 1.3rem;
}

footer .footer-links .footer-link li:hover{
    color: rgba(0, 0, 0, 0.9);
}

footer p{
    /* margin-top: 2rem; */
    background: #f9f9f9;
    padding-top: 10px;
    text-align: center;
    color: #0f0f0f;
    font-size: 1.3rem;
}


</style>