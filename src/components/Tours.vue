<script setup>

</script>

<template>
    <!-- ================================
    START HERO-WRAPPER AREA
    ================================= -->
    <section class="hero-wrapper hero-wrapper7">
        <div class="hero-box hero-bg-6" style="background-image: url(/assets/images/banner_tour.jpg)">
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
        <form action="tours_search.php" method="post" class="row align-items-center">
            <div class="col-lg-3 pr-0">
                <div class="input-box">
                    <label class="label-text">Country</label>
                    <div class="form-group">
                        <span class="la la-map-marker form-icon"></span>
                        <select class="form-control" id="tourCountry" name="tourCountry">
                            <option>Please select a country</option>
                            <option value="13063">United Arab Emirates</option><option value="13069">Austria</option><option value="13070">Australia</option><option value="13072">Azerbaijan</option><option value="13101">Czech Republic</option><option value="15377">France</option><option value="15379">United Kingdom</option><option value="15381">Georgia</option><option value="15388">Greece</option><option value="15391">Hong Kong</option><option value="15395">Hungary</option><option value="15399">India</option><option value="15403">Italy</option><option value="15434">Macau</option><option value="15439">Maldives</option><option value="15442">Malaysia</option><option value="15449">Netherlands</option><option value="15453">Oman</option><option value="15459">Pakistan</option><option value="15465">Qatar</option><option value="15471">Saudi Arabia</option><option value="15474">Singapore</option><option value="15486">Thailand</option><option value="15497">United States</option><option value="15508">South Africa</option>                    </select>
                    </div>
                </div>
            </div>
            <div class="col-lg-3 pr-0">
                <div class="input-box">
                    <label class="label-text">City</label>
                    <div class="form-group">
                        <span class="la la-map-marker form-icon"></span>
                        <select class="form-control" id="tourCity" name="tourCity">
                            <option>Please select a country first</option>
                        </select>
                    </div>
                </div>
            </div>
            <div class="col-lg-3 pr-0">
                <div class="input-box">
                    <label class="label-text">Date</label>
                    <div class="form-group">
                        <span class="la la-calendar form-icon"></span>
                        <input class="date-range form-control" type="text" name="daterange-single" readonly>
                    </div>
                </div>
            </div>
            <div class="col-lg-3">
                <input type="submit" class="theme-btn w-100 text-center margin-top-20px" value="Search" />
            </div>
        </form>
    </div>                    </div>
                    </div><!-- end col-lg-12 -->
                </div><!-- end row -->
            </div><!-- end container -->
        </div>
    </section><!-- end hero-wrapper -->
    <!-- ================================
        END HERO-WRAPPER AREA
    ================================= -->


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
