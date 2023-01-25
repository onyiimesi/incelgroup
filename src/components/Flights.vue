<script setup>

</script>

<template>
    <section class="hero-wrapper hero-wrapper6">
      <div class="hero-box hero-bg-6" style="background-image: url(/assets/images/banner_flight.jpg)">
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
                          </div>
                          </div>
                          </div>
                          <div class="row">
                        <div class="col-lg-12">
                          <div class="search-fields-container mt-4">
                            <div class="section-tab section-tab-2 pb-3">
                              <ul class="nav nav-tabs" id="myTab3" role="tablist">
                                  <li class="nav-item">
                                      <a class="nav-link active" id="one-way-tab" data-toggle="tab" href="#one-way" role="tab" aria-controls="one-way" aria-selected="true">
                                          One way
                                      </a>
                                  </li>
                                  <li class="nav-item">
                                      <a class="nav-link" id="round-trip-tab" data-toggle="tab" href="#round-trip" role="tab" aria-controls="round-trip" aria-selected="false">
                                          Round-trip
                                      </a>
                                  </li>
                                  <!-- <li class="nav-item">
                                      <a class="nav-link" id="multi-city-tab" data-toggle="tab" href="#multi-city" role="tab" aria-controls="multi-city" aria-selected="false">
                                          Multi-city
                                      </a>
                                  </li> -->
                              </ul>
                            </div><!-- end section-tab -->
                            <div class="tab-content" id="myTabContent3">
                              <div class="tab-pane fade show active" id="one-way" role="tabpanel" aria-labelledby="one-way-tab">
                                <div class="contact-form-action">
                                  <form action="flights_search.php" class="row align-items-center" method="post">
                                      <input type="hidden" name="search_type" value="oneway" />
                                      <div class="col-lg-6 pr-0">
                                          <div class="input-box">
                                              <label class="label-text">Flying from</label>
                                              <div class="form-group">
                                                  <span class="la la-map-marker form-icon"></span>
                                                  <input class="form-control" type="text" placeholder="City or airport" name="flight_from" id="flight_from1" autocomplete="on">
                                                  <input type="hidden" name="from" id="from1" value="" />
                                              </div>
                                          </div>
                                      </div>
                                      <div class="col-lg-6">
                                          <div class="input-box">
                                              <label class="label-text">Flying to</label>
                                              <div class="form-group">
                                                  <span class="la la-map-marker form-icon"></span>
                                                  <input class="form-control" type="text" placeholder="City or airport" name="flight_to" id="flight_to1" autocomplete="on">
                                                  <input type="hidden" name="to" id="to1" value="" />
                                              </div>
                                          </div>
                                      </div>
                                      <div class="col-lg-5 pr-0">
                                          <div class="input-box">
                                              <label class="label-text">Departing</label>
                                              <div class="form-group">
                                                  <span class="la la-calendar form-icon"></span>
                                                  <input class="date-range form-control" type="text" name="daterange-single" readonly>
                                              </div>
                                          </div>
                                      </div>
                                      <div class="col-lg-5 pr-0">
                                          <div class="input-box">
                                              <label class="label-text">Passengers</label>
                                              <div class="form-group">
                                                  <div class="dropdown dropdown-contain gty-container">
                                                      <a class="dropdown-toggle dropdown-btn" href="#" role="button" data-toggle="dropdown" aria-expanded="false">
                                                          <span class="adult" data-text="Adult" data-text-multi="Adults">0 Adult</span>
                                                          -
                                                          <span class="children" data-text="Child" data-text-multi="Children">0 Children</span>
                                                      </a>
                                                      <div class="dropdown-menu dropdown-menu-wrap">
                                                          <div class="dropdown-item">
                                                              <div class="qty-box d-flex align-items-center justify-content-between">
                                                                  <label>Adults</label>
                                                                  <div class="qtyBtn d-flex align-items-center">
                                                                      <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                      <input type="text" name="adult_number" value="1">
                                                                      <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                  </div>
                                                              </div>
                                                          </div>
                                                          <div class="dropdown-item">
                                                              <div class="qty-box d-flex align-items-center justify-content-between">
                                                                  <label>Children</label>
                                                                  <div class="qtyBtn d-flex align-items-center">
                                                                      <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                      <input type="text" name="child_number" value="0">
                                                                      <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                  </div>
                                                              </div>
                                                          </div>
                                                          <div class="dropdown-item">
                                                              <div class="qty-box d-flex align-items-center justify-content-between">
                                                                  <label>Infants</label>
                                                                  <div class="qtyBtn d-flex align-items-center">
                                                                      <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                      <input type="text" name="infants_number" value="0" class="qty-input">
                                                                      <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                  </div>
                                                              </div>
                                                          </div>
                                                      </div>
                                                  </div><!-- end dropdown -->
                                              </div>
                                          </div>
                                      </div>
                                      <div class="col-lg-2">
                                          <router-link to="/flight-search-result"><input type="submit" class="theme-btn w-100 text-center margin-top-20px" value="Search" /></router-link>
                                      </div>
                                  </form>
                                  </div>


                                </div><!-- end tab-pane -->
                                  <div class="tab-pane fade" id="round-trip" role="tabpanel" aria-labelledby="round-trip-tab">
                                    <div class="contact-form-action">
                                      <form action="" class="row align-items-center" method="post">
                                          <input type="hidden" name="search_type" value="roundtrip" />

                                          <div class="col-lg-6 pr-0">
                                              <div class="input-box">
                                                  <label class="label-text">Flying from</label>
                                                  <div class="form-group">
                                                      <span class="la la-map-marker form-icon"></span>
                                                      <input class="form-control select2-input" type="text" placeholder="City or airport" name="flight_from" id="flight_from2" autocomplete="on">
                                                      <input type="hidden" name="from" id="from2" value="" />
                                                  </div>
                                              </div>
                                          </div>
                                          <div class="col-lg-6">
                                          <div class="input-box">
                                                  <label class="label-text">Flying to</label>
                                                  <div class="form-group">
                                                      <span class="la la-map-marker form-icon"></span>
                                                      <input class="form-control" type="text" placeholder="City or airport" name="flight_to" id="flight_to2" autocomplete="on">
                                                      <input type="hidden" name="to" id="to2" value="" />
                                                  </div>
                                              </div>
                                          </div>
                                          <div class="col-lg-4 pr-0">
                                              <div class="input-box">
                                                  <label class="label-text">Departing - Returning</label>
                                                  <div class="form-group">
                                                      <span class="la la-calendar form-icon"></span>
                                                      <input class="date-range form-control" type="text" name="daterange" readonly>
                                                  </div>
                                              </div>
                                          </div>
                                          <div class="col-lg-3 pr-0">
                                              <div class="input-box">
                                                  <label class="label-text">Passengers</label>
                                                  <div class="form-group">
                                                      <div class="dropdown dropdown-contain gty-container">
                                                          <a class="dropdown-toggle dropdown-btn" href="#" role="button" data-toggle="dropdown" aria-expanded="false">
                                                              <span class="adult" data-text="Adult" data-text-multi="Adults">0 Adult</span>
                                                              -
                                                              <span class="children" data-text="Child" data-text-multi="Children">0 Children</span>
                                                          </a>
                                                          <div class="dropdown-menu dropdown-menu-wrap">
                                                              <div class="dropdown-item">
                                                                  <div class="qty-box d-flex align-items-center justify-content-between">
                                                                      <label>Adults</label>
                                                                      <div class="qtyBtn d-flex align-items-center">
                                                                          <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                          <input type="text" name="adult_number" value="1">
                                                                          <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                      </div>
                                                                  </div>
                                                              </div>
                                                              <div class="dropdown-item">
                                                                  <div class="qty-box d-flex align-items-center justify-content-between">
                                                                      <label>Children</label>
                                                                      <div class="qtyBtn d-flex align-items-center">
                                                                          <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                          <input type="text" name="child_number" value="0">
                                                                          <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                      </div>
                                                                  </div>
                                                              </div>
                                                              <div class="dropdown-item">
                                                                  <div class="qty-box d-flex align-items-center justify-content-between">
                                                                      <label>Infants</label>
                                                                      <div class="qtyBtn d-flex align-items-center">
                                                                          <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                          <input type="text" name="infants_number" value="0" class="qty-input">
                                                                          <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                      </div>
                                                                  </div>
                                                              </div>
                                                          </div>
                                                      </div><!-- end dropdown -->
                                                  </div>
                                              </div>
                                          </div>
                                          <div class="col-lg-3">
                                              <div class="input-box">
                                                  <label class="label-text">Coach</label>
                                                  <div class="form-group">
                                                      <div class="select-contain w-auto">
                                                          <select class="select-contain-select from-select" name="flight_option">
                                                              <option value="FSC" selected>Direct Flights</option>
                                                              <option value="OWC">Flexible Flights</option>
                                                          </select>
                                                      </div>
                                                  </div>
                                              </div>
                                          </div>
                                          <div class="col-lg-2">
                                              <router-link to="/flight-search-result"><input type="submit" class="theme-btn w-100 text-center margin-top-20px" value="Search" /></router-link>
                                          </div>

                                      </form>
                                    </div>   
                                  </div>
                                </div>
                                <div class="tab-pane fade multi-flight-wrap" id="multi-city" role="tabpanel" aria-labelledby="multi-city-tab">
                                </div>
                          
                          
                      </div><!-- end search-result-content -->
                  </div><!-- end col-lg-12 -->
              </div><!-- end row -->
          </div><!-- end container -->
      </div><!-- end breadcrumb-wrap -->
      <div class="bread-svg-box">
          <svg class="bread-svg" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 10" preserveAspectRatio="none"><polygon points="100 0 50 10 0 0 0 10 100 10"></polygon></svg>
      </div><!-- end bread-svg -->
  </section>


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
