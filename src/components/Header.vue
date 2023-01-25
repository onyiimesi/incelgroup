<template>

    <!-- start cssload-loader -->
  <!-- <div class="preloader" id="preloader">
      <div class="loader">
          <svg class="spinner" viewBox="0 0 50 50">
              <circle class="path" cx="25" cy="25" r="20" fill="none" stroke-width="5"></circle>
          </svg>
      </div>
  </div> -->
  <!-- end cssload-loader -->

  <header class="header-area">
    <div class="header-top-bar padding-right-100px padding-left-100px">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <div class="header-top-content">
                        <div class="header-left">
                            <ul class="list-items">
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="header-top-content">
                        <div class="header-right d-flex align-items-center justify-content-end">
                            <div class="w-auto">
                                <button class="theme-btn theme-btn-small dropdown-toggle mr-4" type="button" id="currency_selector" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                    AED                                </button>
                                <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                                    <a class="dropdown-item" href="switcher_currency.php?return_url=https%3A%2F%2Fportaltest.incelgroup.com%2Findex.php&currency_code=AED">AED</a>
                                    <a class="dropdown-item" href="switcher_currency.php?return_url=https%3A%2F%2Fportaltest.incelgroup.com%2Findex.php&currency_code=USD">USD</a>
                                    <a class="dropdown-item" href="switcher_currency.php?return_url=https%3A%2F%2Fportaltest.incelgroup.com%2Findex.php&currency_code=NGN">NGN</a>
                                </div>
                            </div>
                            <div class="header-right-action">
                                <a href="#" class="theme-btn theme-btn-small theme-btn-transparent mr-1" data-toggle="modal" data-target="#signupPopupForm">Sign Up</a>
                                <a href="#" class="theme-btn theme-btn-small" data-toggle="modal" data-target="#loginPopupForm">Login</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="header-menu-wrapper padding-right-100px padding-left-100px">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="menu-wrapper">
                        <a href="#" class="down-button"><i class="la la-angle-down"></i></a>
                        <div class="logo pb-2">
                            <router-link to="/"><img src="https://www.inceltourism.com/wp-content/uploads/2017/09/incellogo.jpg" alt="logo"></router-link>
                            <div class="menu-toggler">
                                <i class="lnr lnr-menu"></i>
                                <!-- <i class="lnr lnr-cross"></i> -->
                            </div><!-- end menu-toggler -->
                        </div><!-- end logo -->
                        <div class="main-menu-content">
                            <nav>
                                <ul>
                                    <li>
                                      <router-link to="/"><i class="lnr lnr-home"></i> Home</router-link>
                                    </li>
                                    <li>
                                      <router-link to="/flights"><i class="lnr lnr-rocket"></i> Flights</router-link>
                                    </li>
                                    <li>
                                      <router-link to="/hotels"><i class="lnr lnr-apartment"></i> Hotels</router-link>
                                    </li>
                                    <li>
                                      <router-link to="/tours"><i class="lnr lnr-earth"></i> Tours</router-link>
                                    </li>
                                    <li>
                                      <router-link to="/visas"><i class="lnr lnr-earth"></i> Visas</router-link>
                                    </li>
                                    <li>
                                      <router-link to="/careers"><i class="lnr lnr-briefcase"></i> Careers</router-link>
                                    </li>
                                    <li>
                                      <router-link to="/contact"><i class="lnr lnr-phone-handset"></i> Contact</router-link>
                                    </li>
                                </ul>
                            </nav>
                        </div><!-- end main-menu-content -->
                    </div><!-- end menu-wrapper -->
                </div><!-- end col-lg-12 -->
            </div><!-- end row -->
        </div><!-- end container-fluid -->
    </div><!-- end header-menu-wrapper -->
</header>

  

</template>