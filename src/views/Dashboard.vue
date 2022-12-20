<template>
    <Navbar></Navbar>
    <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel"  ref="infoBox">
        <div class="carousel-indicators">
            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active"
                aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1"
                aria-label="Slide 2"></button>
            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2"
                aria-label="Slide 3"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="3"
                aria-label="Slide 4"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="4"
                aria-label="Slide 5"></button>
        </div>
        <div class="carousel-inner">
            <div class="carousel-item active">
                <img src="../images/carousel_1.jpg" class="d-block w-100" alt="..." @load="gethight">
            </div>
            <div class="carousel-item">
                <img src="../images/carousel_2.jpg" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
                <img src="../images/carousel_3.jpg" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
                <img src="../images/carousel_4.jpg" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
                <img src="../images/carousel_5.jpg" class="d-block w-100" alt="...">
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators"
            data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators"
            data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
    <div id="cardbox" class="container-fluid ">
        <div class="row justify-content-center">
            <div class="col-md-3 col-6 card-mt">
                <div class="card">
                    <img src="../images/Venice_1.jpg" class="card-img-top" alt="...">
                    <div class="card-img-overlay card-boxtitle">
                        <p class="card-text text-light bg-dark ">威尼斯</p>
                    </div>
                </div>
            </div>
            <div class="col-md-3 col-6 card-mt">
                <div class="card">
                    <img src="../images/D01_1.jpg" class="card-img-top" alt="...">
                    <div class="card-img-overlay card-boxtitle">
                        <p class="card-text text-light bg-dark ">
                            D01
                        </p>
                    </div>
                </div>
            </div>
            <div class="col-md-3 col-6 card-mt">
                <div class="card">
                    <img src="../images/tesla_1.jpg" class="card-img-top" alt="...">
                    <div class="card-img-overlay card-boxtitle">
                        <p class="card-text text-light bg-dark ">
                            特斯拉
                        </p>
                    </div>
                </div>
            </div>
            <div class="col-md-3 col-6 card-mt">
                <div class="card">
                    <img src="../images/Ennio_1.jpg" class="card-img-top" alt="...">
                    <div class="card-img-overlay card-boxtitle">
                        <p class="card-text text-light bg-dark ">
                            恩尼奧
                        </p>
                    </div>
                </div>
            </div>
            <div class="col-md-3 col-6 card-mt">
            <div class="card">
                <img src="../images/bed_1.jpg" class="card-img-top" alt="...">
                <div class="card-img-overlay card-boxtitle">
                    <p class="card-text text-light bg-dark ">
                        床組
                    </p>
                </div>
            </div>
            </div>
        </div>
    </div>
    <footerview></footerview>
</template>
<style>
.card-mt{
    margin-top: 10px;
}
.card-boxtitle{
    cursor: pointer;
}
.card-boxtitle p{
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 30px;
    opacity: 0;
    transition: opacity 1s;
}
.card-boxtitle:hover p{
    opacity: 1;
}
</style>
<script>
import Navbar from '../components/Navbar.vue';
import footerview from '../components/FooterView.vue';
export default {
    name: 'Dashboard',
    components: {
        Navbar,
        footerview
    },
    methods: {
        gethight () {
            const carousel = document.getElementById('carouselExampleIndicators').offsetHeight;
            const footer = document.getElementById('footerid').offsetHeight;
            const header = document.getElementById('navbarid').offsetHeight;
            const cardbox = document.getElementById('cardbox');
            const heighttotall = carousel + footer + header;
            cardbox.style.cssText = `min-height:calc(100vh - ${heighttotall}px)`;
            console.log(carousel + footer + header);
        }
    }
};
</script>
