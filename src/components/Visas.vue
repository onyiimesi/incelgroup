<script setup>

</script>

<template>
    <!-- ================================
    START HERO-WRAPPER AREA
    ================================= -->
    <section class="hero-wrapper hero-wrapper7" style="background:url(/assets/images/banner_visa.jpg)">
        <div class="hero-box">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="hero-content">
                            <div class="section-heading">
                                <h2 class="sec__title cd-headline slide d-flex align-items-center">
                                    It's the Time to
                                    <span class="cd-words-wrapper pl-2">
                                    <b class="is-visible">discover</b>
                                    <b>fly far</b>
                                    <b>explore</b>
                                    <b>travel</b>
                                    <b>meet</b>
                                    <b>have fun</b>
                                    <b>run away</b>
                                    <b>rejuvenate</b>
                                    <b>live</b>
                                    <b>relax</b>
                                    <b>enjoy life</b>
                                    </span>
                                </h2>
                            </div>
                        </div><!-- end hero-content -->
                    </div><!-- end col-lg-12 -->
                </div><!-- end row -->
                <div class="row">
                    <div class="col-lg-12">
                        <div class="search-fields-container">
                            <div class="contact-form-action">
        <form action="visas_search.php" method="post" class="row align-items-center">
            <div class="col-lg-5 pr-0">
                <div class="input-box">
                    <label class="label-text">Destination</label>
                    <div class="form-group">
                        <span class="la la-map-marker form-icon"></span>
                        <select class="form-control" id="tourVisa" name="country_destination">
                            <option>Please select a country</option>
                            <option value="ARE">UNITED ARAB EMIRATES</option>                    </select>
                    </div>
                </div>
            </div>
            <!--<div class="col-lg-3 pr-0">
                <div class="input-box">
                    <label class="label-text">Nationality</label>
                    <div class="form-group">
                        <span class="la la-map-marker form-icon"></span>
                        <select class="form-control" id="tourVisa" name="country_nationality">
                            <option>Please select a country</option>
                                                </select>
                    </div>
                </div>
            </div>
            <div class="col-lg-3 pr-0">
                <div class="input-box">
                    <label class="label-text">Country of Residence</label>
                    <div class="form-group">
                        <span class="la la-map-marker form-icon"></span>
                        <select class="form-control" id="tourVisa" name="country_residence">
                            <option>Please select a country</option>
                                                </select>
                    </div>
                </div>
            </div>-->
            <div class="col-lg-5">
                <div class="input-box">
                    <label class="label-text">Guests</label>
                    <div class="form-group">
                        <div class="dropdown dropdown-contain gty-container">
                            <a class="dropdown-toggle dropdown-btn" href="#" role="button" data-toggle="dropdown" aria-expanded="false">
                                <span class="adult" data-text="Person" data-text-multi="Persons">0 Persons</span>
                                <!---
                                <span class="children" data-text="Child" data-text-multi="Children">0 Children</span>-->
                            </a>
                            <div class="dropdown-menu dropdown-menu-wrap">
                                <div class="dropdown-item">
                                    <div class="qty-box d-flex align-items-center justify-content-between">
                                        <label>Persons</label>
                                        <div class="qtyBtn d-flex align-items-center">
                                            <div class="qtyDec"><i class="la la-minus"></i></div>
                                            <input type="text" name="adult_number" value="0">
                                            <div class="qtyInc"><i class="la la-plus"></i></div>
                                        </div>
                                    </div>
                                </div>
                                <!--<div class="dropdown-item">
                                    <div class="qty-box d-flex align-items-center justify-content-between">
                                        <label>Children</label>
                                        <div class="qtyBtn d-flex align-items-center">
                                            <div class="qtyDec"><i class="la la-minus"></i></div>
                                            <input type="text" name="child_number" value="0">
                                            <div class="qtyInc"><i class="la la-plus"></i></div>
                                        </div>
                                    </div>
                                </div>-->
                            </div>
                        </div><!-- end dropdown -->
                    </div>
                </div>
            </div>
            <div class="col-lg-2">
                <input type="submit" class="theme-btn w-100 text-center margin-top-20px" value="Search" />
            </div>
        </form>
    </div>
                        </div>
                    </div><!-- end col-lg-12 -->
                </div><!-- end row -->
            </div><!-- end container -->
        </div>
    </section><!-- end hero-wrapper -->
    <!-- ================================
        END HERO-WRAPPER AREA
    ================================= -->
    <div class="section-block"></div>


   <!-- ================================
       START FOOTER AREA
    ================================= -->
    <section class="footer-area section-bg padding-top-100px padding-bottom-30px">
        <div class="container">
            <div class="row">
                <div class="col-lg-4 responsive-column">
                    <div class="footer-item">
                        <div class="footer-logo padding-bottom-30px">
                            <router-link to="/"><img src="/assets/images/logo.png" alt="logo"></router-link>
                        </div><!-- end logo -->
                        
                    </div><!-- end footer-item -->
                </div><!-- end col-lg-3 -->
                <div class="col-lg-4 responsive-column">
                    <div class="footer-item">
                        <h4 class="title curve-shape pb-3 margin-bottom-20px">Dubia</h4>
                        <p>
                          Suite 403, Dubai National Insurance BLDG, Opposite Deira City Center, Dubai, United Arab Emirates.
                        </p>
                        <p>+971 50 149 6155</p>
                        <a href="mailto:enquiries@inceltourism.com">enquiries@inceltourism.com</a>
                    </div><!-- end footer-item -->
                </div><!-- end col-lg-3 -->
                <div class="col-lg-4 responsive-column">
                    <div class="footer-item">
                        <h4 class="title curve-shape pb-3 margin-bottom-20px">Lagos</h4>
                        <p class="footer__desc pb-3">
                          3rd Floor, Sea-Wing Foreshore Towers 2A, Osborne Road, Ikoyi, Lagos, Nigeria.
                        </p>
                        <p>+234 708 859 9941</p>
                        <a href="mailto:enquiries@inceltourism.com">enquiries@inceltourism.com</a>
                    </div><!-- end footer-item -->
                </div><!-- end col-lg-3 -->
            </div><!-- end row -->
            <div class="row align-items-center">
                <div class="col-lg-8">
                    <div class="term-box footer-item">
                        <ul class="list-items list--items d-flex align-items-center">
                            <li><a href="#">Terms & Conditions</a></li>
                            <li><a href="#">Privacy Policy</a></li>
                        </ul>
                    </div>
                </div><!-- end col-lg-8 -->
                <div class="col-lg-4">
                    <div class="footer-social-box text-right">
                        <ul class="social-profile">
                            <li><a href="#"><i class="lab la-facebook-f"></i></a></li>
                            <li><a href="#"><i class="lab la-twitter"></i></a></li>
                            <li><a href="#"><i class="lab la-instagram"></i></a></li>
                            <li><a href="#"><i class="lab la-linkedin-in"></i></a></li>
                        </ul>
                    </div>
                </div><!-- end col-lg-4 -->
            </div><!-- end row -->
        </div><!-- end container -->
        <div class="section-block mt-4"></div>
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-7">
                    <div class="copy-right padding-top-30px">
                        <p class="copy__desc">
                            &copy; Copyright 2022. Powered by <a href="https://ibsnigeria.com/">Intelligence</a>
                        </p>
                    </div><!-- end copy-right -->
                </div><!-- end col-lg-7 -->
                <div class="col-lg-5">
                    <div class="copy-right-content d-flex align-items-center justify-content-end padding-top-30px">
                        <h3 class="title font-size-15 pr-2">We Accept</h3>
                        <img src="/assets/images/payment-img.png" alt="">
                    </div><!-- end copy-right-content -->
                </div><!-- end col-lg-5 -->
            </div><!-- end row -->
        </div><!-- end container -->
    </section><!-- end footer-area -->
    <!-- ================================
          START FOOTER AREA
    ================================= -->


</template>

<style scoped>

</style>
