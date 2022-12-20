<template>
    <!-- <div class="fixed-bottom"> -->
    <!-- <div class="container-fluid bg-success bg-gradient footer-wd d-flex ">
        <footer class="d-flex flex-wrap justify-content-between align-items-center ">
            <div class="col-md-4 d-flex align-items-center">
                <span class="text-light">© 2022 wu_zong_xun</span>
            </div>
            <ul class="nav col-md-4 justify-content-end list-unstyled d-flex">
                <li class="ms-3"><a class="text-light fs-3" href="#"><i class="bi bi-instagram"></i></a></li>
                <li class="ms-3"><a class="text-light fs-3" href="#"><i class="bi bi-facebook"></i></a></li>
                <li class="ms-3"><a class="text-light fs-3" href="#"><i class="bi bi-twitter"></i></a></li>
            </ul>
        </footer>
    </div> -->
    <footer id="footerid" class=" text-center text-white bg-success bg-gradient ">
        <div class="container p-4 pb-0">
            <section class="mb-4">
                <a class="btn btn-outline-light btn-floating m-1" href="#" role="button"><i class="bi bi-instagram"></i></a>
                <a class="btn btn-outline-light btn-floating m-1" href="#" role="button"><i class="bi bi-facebook"></i></a>
                <a class="btn btn-outline-light btn-floating m-1" href="#" role="button"><i class="bi bi-twitter"></i></a>
            </section>
        </div>

        <!-- Copyright -->
        <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2);">
            © 2020 wu_zong_xun
        </div>
        <!-- Copyright -->
    </footer>
    <!-- </div> -->
</template>
<style>
.footer-wd {
    height: 74px;
    flex-direction: column;
    justify-content: center;
    /* position: absolute;
    bottom: 0; */
}
</style>
<script>
export default {
    mounted () {
        this.$nextTick(function () {
            const carousel = document.getElementById('footerid').offsetHeight;
            console.log(carousel);
        });
    }
};
</script>
