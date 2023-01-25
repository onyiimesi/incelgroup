<script>

    import axios from 'axios'

    export default{
        data(){
            return{
                from: '',
                to: '',
                departuredate: '',
                adults: '',
                child: '',
                infants: '',

                showsearch: false,
                caris: []
            }
        },

        methods: {
            async handleSearch(){
                await axios.post('https://incelgroup.com/test/API/flights_search_result.php?session_code=flight6231927836c33')
                .then(res => {
                    this.caris = res;
                    this.from = '';
                    this.showsearch = true;
                })
                .catch(err => {
                    console.log(err);
                })
            }
        }
    }

    // export default{
    //     name: 'viewbanks',
        
    //     data(){
    //         return{
    //             name: '',
    //             caris: [],
    //             showsearch: false,
    //         }
    //     },

    //     async mounted(){
    //         const result = await axios.get('https://portaltest.incelgroup.com/flights_search_result.php?session_code=flight62d00a5ab331e');
    //         this.caris = result.Search_Result;

    //         console.log(result);
    //         this.showsearch = true;
    //     },
    // }
</script>

<template>
  
    <!-- ================================
    START HERO-WRAPPER AREA
    ================================= -->
    <div v-if="showsearch == true" class="container mt-3 mb-5">
        <div class="row">
            <div class="col-lg-12">
                <div class="card">
                    <div class="card-body">
                        <p>
                            One way flight from  to  for Adults 1, Children 1, Infants 1 on 2022-07-08 
                        </p>               
                    </div>
                </div>
            </div>
            <div class="col-lg-12 mt-4">
                <div class="row">
                    <div class="col-md-3">
                        <div class="filters">
                            
                            <div class="accordion mb-3" id="accordionExample">
                                <div class="card">
                                    <div class="card-header" id="headingOne">
                                        <h2 class="mb-0">
                                            <button class="btn btn-link btn-block text-left" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                                            Airlines
                                            </button>
                                        </h2>
                                    </div>

                                    <div id="collapseOne" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
                                        <div class="card-body">
                                            <form>
                                                <div class="mb-2">
                                                    <input type="checkbox"> <span style="padding-left: 5px;font-size: 16px;font-weight: 600;">Air Peace</span> 
                                                    <span style="padding-left: 5px;font-size: 12px;">₦51,692</span>
                                                </div>

                                                <div class="mb-2">
                                                    <input type="checkbox"> <span style="padding-left: 5px;font-size: 16px;font-weight: 600;">Air Peace</span> 
                                                    <span style="padding-left: 5px;font-size: 12px;">₦51,692</span>
                                                </div>

                                                <div class="mb-2">
                                                    <input type="checkbox"> <span style="padding-left: 5px;font-size: 16px;font-weight: 600;">Air Peace</span> 
                                                    <span style="padding-left: 5px;font-size: 12px;">₦51,692</span>
                                                </div>

                                                <div class="mb-2">
                                                    <input type="checkbox"> <span style="padding-left: 5px;font-size: 16px;font-weight: 600;">Air Peace</span> 
                                                    <span style="padding-left: 5px;font-size: 12px;">₦51,692</span>
                                                </div>
                                            </form>
                                        </div>
                                    </div>
                                </div>
                                
                            </div>

                            <div class="accordion mb-3" id="accordionExample">
                                <div class="card">
                                    <div class="card-header" id="headingTwo">
                                        <h2 class="mb-0">
                                            <button class="btn btn-link btn-block text-left" type="button" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="true" aria-controls="collapseTwo">
                                            Airports
                                            </button>
                                        </h2>
                                    </div>

                                    <div id="collapseTwo" class="collapse show" aria-labelledby="headingTwo" data-parent="#accordionExample">
                                        <div class="card-body">
                                            <form>
                                                <div class="mb-2">
                                                    <span style="padding-left: 5px;font-size: 14px;font-weight: 600;">Lagos</span><br>
                                                    <input type="checkbox">  
                                                    <span> LOS: Murtala Moha</span>
                                                    <span style="padding-left: 5px;font-size: 12px;">₦51,692</span>
                                                </div>

                                                <div class="mb-2">
                                                    <span style="padding-left: 5px;font-size: 14px;font-weight: 600;">Abuja</span><br>
                                                    <input type="checkbox">  
                                                    <span> Abuja</span>
                                                    <span style="padding-left: 5px;font-size: 12px;">₦51,692</span>
                                                </div>

                                            </form>
                                        </div>
                                    </div>
                                </div>
                                
                            </div>
                        </div>
                    </div>

                    <div class="col-md-9">
                       <div class="flightSer border shadow-sm " v-for="cari in caris">
                            <div class="row text-center mb-3" type="button" data-toggle="collapse" data-target="#collapseExample">
                                <div class="col-md-2 mt-3">
                                    <span>United Nigeria Airlines</span>
                                </div>
                                
                                <div class="col-md-6 mt-3">
                                    <div class="d-flex justify-content-center">
                                        <p class="pr-3"><strong>{{cari.from}}</strong></p>
                                        ------
                                        <p class="pl-4 pr-5">{{cari.from}}</p>
                                    </div>
                                </div>

                                <div class="col-md-1 mt-3">
                                    <p>1h 15m</p>
                                </div>

                                <div class="col-md-3">
                                    <router-link to="/booking"><button class="btn btn-primary p-3">
                                        <h5>N35, 000</h5>
                                        <span style="font-size: 12px;">BOOK NOW</span>
                                    </button></router-link>
                                </div>
                            </div>
                            
                            <div class="collapse" id="collapseExample">
                                <div class="card card-body">
                                    <div class="row">
                                        <div class="col-md-4 border-right">
                                            <div class="flightsearch">
                                                <span style="font-size: 12px;">FROM</span>
                                                <h5 style="padding: 10px 0;font-weight: bold;font-size: 18px;">16 Jul 2022</h5>
                                                <span style="font-size: 12px;">Airport name</span>
                                                <h6 style="padding: 10px 0;font-size: 16px;">10: 55 am</h6>
                                            </div>
                                        </div>

                                        <div class="col-md-8">
                                            <div class="flightsearch">
                                                
                                                <div style="border-bottom: 1px dotted #333;margin: 0 0 10px 0; padding: 0 0 5px 0;">
                                                    <span>To 16 Jul 2022</span>
                                                </div>

                                                <div class="row">
                                                    <div class="col-md-6">
                                                        <h4 style="padding: 10px 0;font-weight: bold;font-size: 18px;">09:20 AM - 10:55 AM</h4>
                                                        <p>
                                                            ABV Abuja Intl
                                                        </p>
                                                        <p>
                                                            LOS Murtala Muhammed Arpt
                                                        </p>
                                                    </div>

                                                    <div class="col-md-6">
                                                        <div class="flightsearch">
                                                            <p>
                                                                <strong>Flight Class</strong> Economy
                                                            </p>
                                                            <p>
                                                                <strong>Trip Duration</strong> 1h 35m Hours
                                                            </p>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div> 
                                        </div>
                                    </div>
                                </div>
                            </div>
                       </div>
                       
                       <!-- <div class="flightSer border shadow-sm ">
                            <div class="row text-center mb-3" type="button" data-toggle="collapse" data-target="#collapseExample1">
                                <div class="col-md-2 mt-3">
                                    <span>United Nigeria Airlines</span>
                                </div>
                                
                                <div class="col-md-6 mt-3">
                                    <div class="d-flex justify-content-center">
                                        <p class="pr-3"><strong>5:00 AM</strong> <br><span>Abj Intl</span><br> LOS</p>
                                        ------
                                        <p class="pl-4 pr-5"><strong>6:15 AM</strong> <br><span>Murtala Muhammed</span><br> ABV</p>
                                    </div>
                                </div>

                                <div class="col-md-1 mt-3">
                                    <p>1h 15m</p>
                                </div>

                                <div class="col-md-3">
                                    <router-link to="/booking"><button class="btn btn-primary p-3">
                                        <h5>N35, 000</h5>
                                        <span style="font-size: 12px;">BOOK NOW</span>
                                    </button></router-link>
                                </div>
                            </div>
                            
                            <div class="collapse" id="collapseExample1">
                                <div class="card card-body">
                                    <div class="row">
                                        <div class="col-md-4 border-right">
                                            <div class="flightsearch">
                                                <span style="font-size: 12px;">FROM</span>
                                                <h5 style="padding: 10px 0;font-weight: bold;font-size: 18px;">16 Jul 2022</h5>
                                                <span style="font-size: 12px;">Airport name</span>
                                                <h6 style="padding: 10px 0;font-size: 16px;">10: 55 am</h6>
                                            </div>
                                        </div>

                                        <div class="col-md-8">
                                            <div class="flightsearch">
                                                
                                                <div style="border-bottom: 1px dotted #333;margin: 0 0 10px 0; padding: 0 0 5px 0;">
                                                    <span>To 16 Jul 2022</span>
                                                </div>

                                                <div class="row">
                                                    <div class="col-md-6">
                                                        <h4 style="padding: 10px 0;font-weight: bold;font-size: 18px;">09:20 AM - 10:55 AM</h4>
                                                        <p>
                                                            ABV Abuja Intl
                                                        </p>
                                                        <p>
                                                            LOS Murtala Muhammed Arpt
                                                        </p>
                                                    </div>

                                                    <div class="col-md-6">
                                                        <div class="flightsearch">
                                                            <p>
                                                                <strong>Flight Class</strong> Economy
                                                            </p>
                                                            <p>
                                                                <strong>Trip Duration</strong> 1h 35m Hours
                                                            </p>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div> 
                                        </div>
                                    </div>
                                </div>
                            </div>
                       </div>

                       <div class="flightSer border shadow-sm ">
                            <div class="row text-center mb-3" type="button" data-toggle="collapse" data-target="#collapseExample2">
                                <div class="col-md-2 mt-3">
                                    <span>United Nigeria Airlines</span>
                                </div>
                                
                                <div class="col-md-6 mt-3">
                                    <div class="d-flex justify-content-center">
                                        <p class="pr-3"><strong>5:00 AM</strong> <br><span>Abj Intl</span><br> LOS</p>
                                        ------
                                        <p class="pl-4 pr-5"><strong>6:15 AM</strong> <br><span>Murtala Muhammed</span><br> ABV</p>
                                    </div>
                                </div>

                                <div class="col-md-1 mt-3">
                                    <p>1h 15m</p>
                                </div>

                                <div class="col-md-3">
                                    <router-link to="/booking"><button class="btn btn-primary p-3">
                                        <h5>N35, 000</h5>
                                        <span style="font-size: 12px;">BOOK NOW</span>
                                    </button></router-link>
                                </div>
                            </div>
                            
                            <div class="collapse" id="collapseExample2">
                                <div class="card card-body">
                                    <div class="row">
                                        <div class="col-md-4 border-right">
                                            <div class="flightsearch">
                                                <span style="font-size: 12px;">FROM</span>
                                                <h5 style="padding: 10px 0;font-weight: bold;font-size: 18px;">16 Jul 2022</h5>
                                                <span style="font-size: 12px;">Airport name</span>
                                                <h6 style="padding: 10px 0;font-size: 16px;">10: 55 am</h6>
                                            </div>
                                        </div>

                                        <div class="col-md-8">
                                            <div class="flightsearch">
                                                
                                                <div style="border-bottom: 1px dotted #333;margin: 0 0 10px 0; padding: 0 0 5px 0;">
                                                    <span>To 16 Jul 2022</span>
                                                </div>

                                                <div class="row">
                                                    <div class="col-md-6">
                                                        <h4 style="padding: 10px 0;font-weight: bold;font-size: 18px;">09:20 AM - 10:55 AM</h4>
                                                        <p>
                                                            ABV Abuja Intl
                                                        </p>
                                                        <p>
                                                            LOS Murtala Muhammed Arpt
                                                        </p>
                                                    </div>

                                                    <div class="col-md-6">
                                                        <div class="flightsearch">
                                                            <p>
                                                                <strong>Flight Class</strong> Economy
                                                            </p>
                                                            <p>
                                                                <strong>Trip Duration</strong> 1h 35m Hours
                                                            </p>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div> 
                                        </div>
                                    </div>
                                </div>
                            </div>
                       </div> -->

                    </div>
                </div>
            </div>
        </div>
    </div>
    <section v-if="showsearch==false" class="hero-wrapper">
        <div class="hero-box hero-bg">
            <span class="line-bg line-bg1"></span>
            <span class="line-bg line-bg2"></span>
            <span class="line-bg line-bg3"></span>
            <span class="line-bg line-bg4"></span>
            <span class="line-bg line-bg5"></span>
            <span class="line-bg line-bg6"></span>
            <div class="container">
                <div class="row">
                    <div class="col-lg-10 mx-auto responsive--column-l">
                        <div class="hero-content pb-5">
                            <div class="section-heading">
                                <h2 class="sec__title cd-headline zoom">
                                    Amazing <span class="cd-words-wrapper">
                                    <b class="is-visible">Tours</b>
                                    <b>Adventures</b>
                                    <b>Flights</b>
                                    <b>Hotels</b>
                                    <b>Cars</b>
                                    <b>Cruises</b>
                                    <b>Package Deals</b>
                                    <b>Fun</b>
                                    <b>People</b>
                                    </span>
                                    Waiting for You
                                </h2>
                            </div>
                        </div><!-- end hero-content -->
                        <div class="section-tab text-center pl-4">
                            <ul class="nav nav-tabs" id="myTab" role="tablist">
                                <li class="nav-item">
                                    <a class="nav-link d-flex align-items-center active" id="flight-tab" data-toggle="tab" href="#flight" role="tab" aria-controls="flight" aria-selected="true">
                                        <i class="la la-plane mr-1"></i>Flights
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a class="nav-link d-flex align-items-center" id="hotel-tab" data-toggle="tab" href="#hotel" role="tab" aria-controls="hotel" aria-selected="false">
                                        <i class="la la-hotel mr-1"></i>Hotels
                                    </a>
                                </li>
                                <!--
                                <li class="nav-item">
                                    <a class="nav-link d-flex align-items-center" id="package-tab" data-toggle="tab" href="#package" role="tab" aria-controls="package" aria-selected="false">
                                        <i class="la la-shopping-bag mr-1"></i>Vacation Packages
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a class="nav-link d-flex align-items-center" id="car-tab" data-toggle="tab" href="#car" role="tab" aria-controls="car" aria-selected="true">
                                        <i class="la la-car mr-1"></i>Cars
                                    </a>
                                </li> -->
                                <li class="nav-item">
                                    <a class="nav-link d-flex align-items-center" id="tour-tab" data-toggle="tab" href="#tour" role="tab" aria-controls="tour" aria-selected="false">
                                        <i class="la la-globe mr-1"></i>Tours
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a class="nav-link d-flex align-items-center" id="visa-tab" data-toggle="tab" href="#visa" role="tab" aria-controls="visa" aria-selected="false">
                                        <i class="la la-globe mr-1"></i>Visas
                                    </a>
                                </li>
                            </ul>
                        </div>
                        <div class="tab-content search-fields-container" id="myTabContent">
                            <div class="tab-pane fade show active" id="flight" role="tabpanel" aria-labelledby="flight-tab">
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
                                </div>
                                <div class="tab-content" id="myTabContent3">
                                    <div class="tab-pane fade show active" id="one-way" role="tabpanel" aria-labelledby="one-way-tab">
                                        <div class="contact-form-action">
                                            <form @submit.prevent="handleSearch" class="row align-items-center">
                                                <input type="hidden" name="search_type" value="oneway" />
                                                <div class="col-lg-6 pr-0">
                                                    <div class="input-box">
                                                        <label class="label-text">Flying from</label>
                                                        <div class="form-group">
                                                            <span class="la la-map-marker form-icon"></span>
                                                            <input class="form-control" type="text" placeholder="City or airport" v-model="from" id="flight_from1" autocomplete="on">
                                                            <input type="hidden" name="from" id="from1" value="" />
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="col-lg-6">
                                                    <div class="input-box">
                                                        <label class="label-text">Flying to</label>
                                                        <div class="form-group">
                                                            <span class="la la-map-marker form-icon"></span>
                                                            <input class="form-control" type="text" placeholder="City or airport" v-model="to" id="flight_to1" autocomplete="on">
                                                            <input type="hidden" name="to" id="to1" value="" />
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="col-lg-5 pr-0">
                                                    <div class="input-box">
                                                        <label class="label-text">Departing</label>
                                                        <div class="form-group">
                                                            <span class="la la-calendar form-icon"></span>
                                                            <input class="date-range form-control" type="text" v-model="departuredate" readonly>
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
                                                                                <input type="text" name="adult_number" value="0">
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
                                                    <!-- <input class="theme-btn w-100 text-center margin-top-20px" value="Search" /> -->
                                                    <button class="theme-btn w-100 text-center margin-top-20px">Search</button>
                                                </div>
                                            </form>
                                        </div>


                                    </div>
                                    <div class="tab-pane fade" id="round-trip" role="tabpanel" aria-labelledby="round-trip-tab">
                                        <div class="contact-form-action">
                                            <form action="flights_search.php" class="row align-items-center" method="post">
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
                                                                <select class="select-contain-select form-select" name="flight_option">
                                                                    <option value="FSC" selected>Direct Flights</option>
                                                                    <option value="OWC">Flexible Flights</option>
                                                                </select>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="col-lg-2">
                                                    <input type="submit" class="theme-btn w-100 text-center margin-top-20px" value="Search" />
                                                </div>

                                            </form>
                                        </div> 
                                    </div>

                                    <div class="tab-pane fade multi-flight-wrap" id="multi-city" role="tabpanel" aria-labelledby="multi-city-tab">
                                </div>
                            </div>
                        </div>
                        <div class="tab-pane fade show" id="hotel" role="tabpanel" aria-labelledby="hotel-tab">
                            <div class="contact-form-action">
                                <form action="hotels_search.php" class="row align-items-center" method="post">
                                    <div class="col-lg-3 pr-0">
                                        <div class="input-box">
                                            <label class="label-text">Country</label>
                                            <div class="form-group">
                                                <span class="la la-map-marker form-icon"></span>
                                                <!-- <input class="form-control" type="text" placeholder="Enter city or property"> -->
                                                <select class="form-control" id="search_hotel_country" name="search_hotel_country">
                                                    <option>Please select a destination</option>
                                                    <option value="AF">Afghanistan</option><option value="AL">Albania</option><option value="DZ">Algeria</option><option value="AS">American Samoa</option><option value="AD">Andorra</option><option value="AO">Angola</option><option value="AI">Anguilla</option><option value="AG">Antigua And Barbuda</option><option value="AR">Argentina</option><option value="AM">Armenia</option><option value="AW">Aruba</option><option value="AU">Australia</option><option value="AT">Austria</option><option value="AZ">Azerbaijan</option><option value="BS">Bahamas</option><option value="BH">Bahrain</option><option value="BD">Bangladesh</option><option value="BB">Barbados</option><option value="BY">Belarus</option><option value="BE">Belgium</option><option value="BZ">Belize</option><option value="BJ">Benin</option><option value="BM">Bermuda</option><option value="BT">Bhutan</option><option value="BO">Bolivia</option><option value="BQ">Bonaire, Sint Eustatius and Saba</option><option value="BA">Bosnia And Herzegovina</option><option value="BW">Botswana</option><option value="BV">Bouvet Island</option><option value="BR">Brazil</option><option value="IO">British Indian Ocean Territory</option><option value="VG">British Virgin Islands</option><option value="BN">Brunei Darussalam</option><option value="BG">Bulgaria</option><option value="BF">Burkina Faso</option><option value="BI">Burundi</option><option value="KH">Cambodia</option><option value="CM">Cameroon</option><option value="CA">Canada</option><option value="CV">Cape Verde</option><option value="KY">Cayman Islands</option><option value="CF">Central African Republic</option><option value="TD">Chad</option><option value="CL">Chile</option><option value="CN">China</option><option value="CX">Christmas Island</option><option value="CC">Cocos Islands</option><option value="CO">Colombia</option><option value="KM">Comoros</option><option value="CK">Cook Islands</option><option value="CR">Costa Rica</option><option value="HR">Croatia</option><option value="CU">Cuba</option><option value="CW">Curacao</option><option value="CY">Cyprus</option><option value="CZ">Czech Republic</option><option value="CD">Democratic Republic of the Congo</option><option value="DK">Denmark</option><option value="DJ">Djibouti</option><option value="DM">Dominica</option><option value="DO">Dominican Republic</option><option value="EC">Ecuador</option><option value="EG">Egypt</option><option value="SV">El Salvador</option><option value="GQ">Equatorial Guinea</option><option value="ER">Eritrea</option><option value="EE">Estonia</option><option value="ET">Ethiopia</option><option value="FK">Falkland Islands</option><option value="FO">Faroe Islands</option><option value="FJ">Fiji</option><option value="FI">Finland</option><option value="FR">France</option><option value="GF">French Guiana</option><option value="PF">French Polynesia</option><option value="TF">French Southern and Antarctic Territories</option><option value="GA">Gabon</option><option value="GM">Gambia</option><option value="GE">Georgia</option><option value="DE">Germany</option><option value="GH">Ghana</option><option value="GI">Gibraltar</option><option value="GR">Greece</option><option value="GL">Greenland</option><option value="GD">Grenada</option><option value="GP">Guadeloupe</option><option value="GU">Guam</option><option value="GT">Guatemala</option><option value="GN">Guinea</option><option value="GW">Guinea-Bissau</option><option value="GY">Guyana</option><option value="HT">Haiti</option><option value="HM">Heard and McDonald Islands</option><option value="HN">Honduras</option><option value="HK">Hong Kong</option><option value="HU">Hungary</option><option value="IS">Iceland</option><option value="IN">India</option><option value="ID">Indonesia</option><option value="IR">Iran</option><option value="IQ">Iraq</option><option value="IE">Ireland</option><option value="IL">Israel</option><option value="IT">Italy</option><option value="CI">Ivory Coast</option><option value="JM">Jamaica</option><option value="JP">Japan</option><option value="JE">Jersey</option><option value="JO">Jordan</option><option value="KZ">Kazakhstan</option><option value="KE">Kenya</option><option value="KI">Kiribati</option><option value="KW">Kuwait</option><option value="KG">Kyrgyzstan</option><option value="LA">Laos</option><option value="LV">Latvia</option><option value="LB">Lebanon</option><option value="LS">Lesotho</option><option value="LR">Liberia</option><option value="LY">Libyan Arab Jamahiriya</option><option value="LI">Liechtenstein</option><option value="LT">Lithuania</option><option value="LU">Luxembourg</option><option value="MO">Macau</option><option value="MK">Macedonia</option><option value="MG">Madagascar</option><option value="MW">Malawi</option><option value="MY">Malaysia</option><option value="MV">Maldives</option><option value="ML">Mali</option><option value="MT">Malta</option><option value="MH">Marshall Islands</option><option value="MQ">Martinique</option><option value="MR">Mauritania</option><option value="MU">Mauritius</option><option value="YT">Mayotte</option><option value="MX">Mexico</option><option value="FM">Micronesia</option><option value="MD">Moldova</option><option value="MC">Monaco</option><option value="MN">Mongolia</option><option value="ME">Montenegro</option><option value="MS">Montserrat</option><option value="MA">Morocco</option><option value="MZ">Mozambique</option><option value="MM">Myanmar</option><option value="NA">Namibia</option><option value="NR">Nauru</option><option value="NP">Nepal</option><option value="NL">Netherlands</option><option value="AN">Netherlands Antilles</option><option value="NC">New Caledonia</option><option value="NZ">New Zealand</option><option value="NI">Nicaragua</option><option value="NE">Niger</option><option value="NG">Nigeria</option><option value="NU">Niue</option><option value="NF">Norfolk Island</option><option value="KP">North Korea</option><option value="MP">Northern Mariana Islands</option><option value="NO">Norway</option><option value="OM">Oman</option><option value="PK">Pakistan</option><option value="PW">Palau</option><option value="PS">Palestinian Territory</option><option value="PA">Panama</option><option value="PG">Papua New Guinea</option><option value="PY">Paraguay</option><option value="PE">Peru</option><option value="PH">Philippines</option><option value="PN">Pitcairn Island</option><option value="PL">Poland</option><option value="PT">Portugal</option><option value="PR">Puerto Rico</option><option value="QA">Qatar</option><option value="CG">Republic of the Congo</option><option value="RE">Reunion</option><option value="RO">Romania</option><option value="RU">Russia</option><option value="RW">Rwanda</option><option value="BL">Saint Barthelemy</option><option value="KN">Saint Kitts And Nevis</option><option value="LC">Saint Lucia</option><option value="MF">Saint Martin</option><option value="VC">Saint Vincent And The Grenadines</option><option value="WS">Samoa</option><option value="SM">San Marino</option><option value="ST">Sao Tome And Principe</option><option value="SA">Saudi Arabia</option><option value="SN">Senegal</option><option value="RS">Serbia</option><option value="SC">Seychelles</option><option value="SL">Sierra Leone</option><option value="SG">Singapore</option><option value="SX">Sint Maarten</option><option value="SK">Slovakia</option><option value="SI">Slovenia</option><option value="SB">Solomon Islands</option><option value="SO">Somalia</option><option value="ZA">South Africa</option><option value="KR">South Korea</option><option value="SS">South Sudan</option><option value="ES">Spain</option><option value="LK">Sri Lanka</option><option value="SH">St. Helena</option><option value="PM">St. Pierre and Miquelon</option><option value="SD">Sudan</option><option value="SR">Suriname</option><option value="SJ">Svalbard And Jan Mayen</option><option value="SZ">Swaziland</option><option value="SE">Sweden</option><option value="CH">Switzerland</option><option value="SY">Syrian Arab Republic</option><option value="TW">Taiwan</option><option value="TJ">Tajikistan</option><option value="TZ">Tanzania</option><option value="TH">Thailand</option><option value="TL">Timor Leste</option><option value="TG">Togo</option><option value="TK">Tokelau</option><option value="TO">Tonga</option><option value="TT">Trinidad And Tobago</option><option value="TN">Tunisia</option><option value="TR">Turkey</option><option value="TM">Turkmenistan</option><option value="TC">Turks And Caicos Islands</option><option value="TV">Tuvalu</option><option value="UG">Uganda</option><option value="UA">Ukraine</option><option value="AE">United Arab Emirates</option><option value="UK">United Kingdom</option><option value="US">United States</option><option value="UY">Uruguay</option><option value="UM">US Minor Outlying Islands</option><option value="VI">US Virgin Islands</option><option value="UZ">Uzbekistan</option><option value="VU">Vanuatu</option><option value="VA">Vatican City</option><option value="VE">Venezuela</option><option value="VN">Vietnam</option><option value="WF">Wallis and Futuna</option><option value="YE">Yemen</option><option value="ZM">Zambia</option><option value="ZW">Zimbabwe</option>                    </select>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-3 pr-0">
                                        <div class="input-box">
                                            <label class="label-text">City</label>
                                            <div class="form-group">
                                                <span class="la la-map-marker form-icon"></span>
                                                <select class="form-control" id="search_hotel_city" name="search_hotel_city">

                                                </select>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-2 pr-0">
                                        <div class="input-box">
                                            <label class="label-text">Check out</label>
                                            <div class="form-group">
                                                <span class="la la-calendar form-icon"></span>
                                                <input class="date-range form-control" type="text" name="daterange" readonly="">
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-2">
                                        <div class="input-box">
                                            <label class="label-text">Guests</label>
                                            <div class="form-group">
                                                <div class="dropdown dropdown-contain gty-container">
                                                    <a class="dropdown-toggle dropdown-btn" href="#" role="button" data-toggle="dropdown" aria-expanded="false">
                                                        <span class="adult" data-text="Adult" data-text-multi="Adults">0 Person(s)</span>
                                                        <span class="children" data-text="Child" data-text-multi="Children">0 Children</span>
                                                    </a>
                                                    <div class="dropdown-menu dropdown-menu-wrap">
                                                        <div class="dropdown-item">
                                                            <div class="qty-box d-flex align-items-center justify-content-between">
                                                                <label>Rooms</label>
                                                                <div class="qtyBtn d-flex align-items-center">
                                                                    <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                    <input type="text" name="room_number" value="0" class="qty-input">
                                                                    <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                </div>
                                                            </div>
                                                        </div>
                                                        <div class="dropdown-item">
                                                            <div class="qty-box d-flex align-items-center justify-content-between">
                                                                <label>Adults</label>
                                                                <div class="qtyBtn d-flex align-items-center">
                                                                    <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                    <input type="text" name="adult_number" value="0">
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
                                                    </div>
                                                </div><!-- end dropdown -->
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-2">
                                        <input type="submit" class="theme-btn w-100 text-center margin-top-20px" value="Search" />
                                    </div>
                                </form>
                            </div>                        </div>
                            <div class="tab-pane fade" id="package" role="tabpanel" aria-labelledby="package-tab">
                                <div class="section-tab section-tab-2 pb-3">
                                    <ul class="nav nav-tabs" id="myTab2" role="tablist">
                                        <li class="nav-item">
                                            <a class="nav-link active" id="flight-hotel-tab" data-toggle="tab" href="#flight-hotel" role="tab" aria-controls="flight-hotel" aria-selected="true">
                                                Flight + Hotel
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" id="flight-hotel-car-tab" data-toggle="tab" href="#flight-hotel-car" role="tab" aria-controls="flight-hotel-car" aria-selected="false">
                                                Flight + Hotel + Car
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" id="flight-car-tab" data-toggle="tab" href="#flight-car" role="tab" aria-controls="flight-car" aria-selected="false">
                                                Flight + Car
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" id="hotel-car-tab" data-toggle="tab" href="#hotel-car" role="tab" aria-controls="hotel-car" aria-selected="true">
                                                Hotel + Car
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                                <div class="tab-content" id="myTabContent2">
                                    <div class="tab-pane fade show active" id="flight-hotel" role="tabpanel" aria-labelledby="flight-hotel-tab">
                                        
                                    <div class="contact-form-action">
                                        <form action="search_vacations.php" method="post" class="row align-items-center">
                                            <div class="col-lg-3 pr-0">
                                                <div class="input-box">
                                                    <label class="label-text">Flying from</label>
                                                    <div class="form-group">
                                                        <span class="la la-map-marker form-icon"></span>
                                                        <input class="form-control" type="text" placeholder="City or airport">
                                                    </div>
                                                </div>
                                            </div><!-- end col-lg-3 -->
                                            <div class="col-lg-3 pr-0">
                                                <div class="input-box">
                                                    <label class="label-text">Flying to</label>
                                                    <div class="form-group">
                                                        <span class="la la-map-marker form-icon"></span>
                                                        <input class="form-control" type="text" placeholder="City or airport">
                                                    </div>
                                                </div>
                                            </div><!-- end col-lg-3 -->
                                            <div class="col-lg-3 pr-0">
                                                <div class="input-box">
                                                    <label class="label-text">Departing - Returning</label>
                                                    <div class="form-group">
                                                        <span class="la la-calendar form-icon"></span>
                                                        <input class="date-range form-control" type="text" name="daterange" readonly>
                                                    </div>
                                                </div>
                                            </div><!-- end col-lg-3 -->
                                            <div class="col-lg-3">
                                                <div class="input-box">
                                                    <label class="label-text">Guests</label>
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
                                                                        <label>Rooms</label>
                                                                        <div class="qtyBtn d-flex align-items-center">
                                                                            <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                            <input type="text" name="room_number" value="0" class="qty-input">
                                                                            <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                        </div>
                                                                    </div>
                                                                </div>
                                                                <div class="dropdown-item">
                                                                    <div class="qty-box d-flex align-items-center justify-content-between">
                                                                        <label>Adults</label>
                                                                        <div class="qtyBtn d-flex align-items-center">
                                                                            <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                            <input type="text" name="adult_number" value="0">
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
                                                            </div>
                                                        </div><!-- end dropdown -->
                                                    </div>
                                                </div>
                                            </div><!-- end col-lg-3 -->
                                        </form>
                                    </div>
                                    <div class="checkmark-wrap">
                                        <div class="custom-checkbox d-inline-block mb-0 mr-3">
                                            <input type="checkbox" id="directFlightChb">
                                            <label for="directFlightChb">Direct flights only</label>
                                        </div>
                                        <div class="custom-checkbox d-inline-block mb-0">
                                            <input type="checkbox" id="onlyHotelChb">
                                            <label for="onlyHotelChb">I only need a hotel for part of my stay</label>
                                        </div>
                                    </div><!-- end checkmark-wrap -->
                                    <div class="btn-box pt-3">
                                        <input type="submit" class="theme-btn" value="Search" />
                                        
                                    </div>  
                                </div>
                                <div class="tab-pane fade" id="flight-hotel-car" role="tabpanel" aria-labelledby="flight-hotel-car-tab">
                                        
                                <div class="contact-form-action">
                                    <form action="search_vacations.php" method="post" class="row align-items-center">
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Flying from</label>
                                                <div class="form-group">
                                                    <span class="la la-map-marker form-icon"></span>
                                                    <input type="text" class="form-control" placeholder="City or airport">
                                                </div>
                                            </div>
                                        </div><!-- end col-lg-3 -->
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Flying to</label>
                                                <div class="form-group">
                                                    <span class="la la-map-marker form-icon"></span>
                                                    <input class="form-control" type="text" placeholder="City or airport">
                                                </div>
                                            </div>
                                        </div><!-- end col-lg-3 -->
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Departing - Returning</label>
                                                <div class="form-group">
                                                    <span class="la la-calendar form-icon"></span>
                                                    <input class="date-range form-control" type="text" name="daterange" readonly>
                                                </div>
                                            </div>
                                        </div><!-- end col-lg-3 -->
                                        <div class="col-lg-3">
                                            <div class="input-box">
                                                <label class="label-text">Guests</label>
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
                                                                    <label>Rooms</label>
                                                                    <div class="qtyBtn d-flex align-items-center">
                                                                        <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                        <input type="text" name="room_number" value="0" class="qty-input">
                                                                        <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                    </div>
                                                                </div>
                                                            </div>
                                                            <div class="dropdown-item">
                                                                <div class="qty-box d-flex align-items-center justify-content-between">
                                                                    <label>Adults</label>
                                                                    <div class="qtyBtn d-flex align-items-center">
                                                                        <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                        <input type="text" name="adult_number" value="0">
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
                                                        </div>
                                                    </div><!-- end dropdown -->
                                                </div>
                                            </div>
                                        </div><!-- end col-lg-3 -->
                                        </form>
                                </div>
                                <div class="checkmark-wrap">
                                    <div class="custom-checkbox d-inline-block mb-0 mr-3">
                                        <input type="checkbox" id="directFlightChb2">
                                        <label for="directFlightChb2">Direct flights only</label>
                                    </div>
                                    <div class="custom-checkbox d-inline-block mb-0">
                                        <input type="checkbox" id="onlyHotelChb2">
                                        <label for="onlyHotelChb2">I only need a hotel for part of my stay</label>
                                    </div>
                                </div><!-- end checkmark-wrap -->
                                <div class="btn-box pt-3">
                                    <input type="submit" class="theme-btn" value="Search" />
                                    
                                </div>
                            </div>
                            <div class="tab-pane fade" id="flight-car" role="tabpanel" aria-labelledby="flight-car-tab">
                                        
                                <div class="contact-form-action">
                                    <form action="search_vacations.php" method="post" class="row align-items-center">
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Flying from</label>
                                                <div class="form-group">
                                                    <span class="la la-map-marker form-icon"></span>
                                                    <input class="form-control" type="text" placeholder="City or airport">
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Flying to</label>
                                                <div class="form-group">
                                                    <span class="la la-map-marker form-icon"></span>
                                                    <input class="form-control" type="text" placeholder="City or airport">
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Departing - Returning</label>
                                                <div class="form-group">
                                                    <span class="la la-calendar form-icon"></span>
                                                    <input class="date-range form-control" type="text" name="daterange" readonly>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-lg-3">
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
                                                                        <input type="text" name="adult_number" value="0">
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
                                    </form>
                                </div>
                                <div class="checkmark-wrap">
                                    <div class="custom-checkbox d-inline-block mb-0">
                                        <input type="checkbox" id="directFlightChb3">
                                        <label for="directFlightChb3">Direct flights only</label>
                                    </div>
                                </div><!-- end checkmark-wrap -->
                                <div class="btn-box pt-3">
                                    <input type="submit" class="theme-btn" value="Search" />
                                    <!-- end row -->
                                </div>   
                            </div>
                            <div class="tab-pane fade" id="hotel-car" role="tabpanel" aria-labelledby="hotel-car-tab">
                                        
                                <div class="contact-form-action">
                                    <form action="search_vacations.php" method="post" class="row align-items-center">
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Going to</label>
                                                <div class="form-group">
                                                    <span class="la la-map-marker form-icon"></span>
                                                    <input class="form-control" type="text" placeholder="Enter City or property">
                                                </div>
                                            </div>
                                        </div><!-- end col-lg-3 -->
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Check in - Check-out</label>
                                                <div class="form-group">
                                                    <span class="la la-calendar form-icon"></span>
                                                    <input class="date-range form-control" type="text" name="daterange" readonly>
                                                </div>
                                            </div>
                                        </div><!-- end col-lg-3 -->
                                        <div class="col-lg-3 pr-0">
                                            <div class="input-box">
                                                <label class="label-text">Room Type</label>
                                                <div class="form-group">
                                                    <div class="select-contain w-auto">
                                                        <select class="select-contain-select">
                                                            <option value="0">Select Type</option>
                                                            <option value="1">Single</option>
                                                            <option value="2">Double</option>
                                                            <option value="3">Triple</option>
                                                            <option value="4">Quad</option>
                                                            <option value="5">Queen</option>
                                                            <option value="6">King</option>
                                                            <option value="7">Twin</option>
                                                            <option value="8">Double-double</option>
                                                            <option value="9">Studio</option>
                                                            <option value="10">Suite</option>
                                                            <option value="11">Mini Suite</option>
                                                            <option value="12">President Suite</option>
                                                            <option value="13">President Suite</option>
                                                            <option value="14">Apartments</option>
                                                            <option value="15">Connecting rooms</option>
                                                            <option value="16">Murphy Room</option>
                                                            <option value="17">Accessible Room</option>
                                                            <option value="18">Cabana</option>
                                                            <option value="19">Adjoining rooms</option>
                                                            <option value="20">Adjacent rooms</option>
                                                            <option value="21">Villa</option>
                                                            <option value="22">Executive Floor</option>
                                                            <option value="23">Smoking room</option>
                                                            <option value="24">Non-Smoking Room</option>
                                                        </select>
                                                    </div>
                                                </div>
                                            </div>
                                        </div><!-- end col-lg-3 -->
                                        <div class="col-lg-3">
                                            <div class="input-box">
                                                <label class="label-text">Guests</label>
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
                                                                    <label>Rooms</label>
                                                                    <div class="qtyBtn d-flex align-items-center">
                                                                        <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                        <input type="text" name="room_number" value="0" class="qty-input">
                                                                        <div class="qtyInc"><i class="la la-plus"></i></div>
                                                                    </div>
                                                                </div>
                                                            </div>
                                                            <div class="dropdown-item">
                                                                <div class="qty-box d-flex align-items-center justify-content-between">
                                                                    <label>Adults</label>
                                                                    <div class="qtyBtn d-flex align-items-center">
                                                                        <div class="qtyDec"><i class="la la-minus"></i></div>
                                                                        <input type="text" name="adult_number" value="0">
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
                                                        </div>
                                                    </div><!-- end dropdown -->
                                                </div>
                                            </div>
                                        </div><!-- end col-lg-3 -->
                                    </form>
                                </div>
                                <div class="btn-box pt-2">
                                    <input type="submit" class="theme-btn" value="Search" />
                                    
                                </div>                                
                            </div>
                        </div>
                    </div>
                    <div class="tab-pane fade" id="car" role="tabpanel" aria-labelledby="car-tab">
                                
                        <div class="contact-form-action">
                            <form action="search_cars.php" method="post" class="row align-items-center">
                                <div class="col-lg-4 pr-0">
                                    <div class="input-box">
                                        <label class="label-text">Picking up</label>
                                        <div class="form-group">
                                            <span class="la la-map-marker form-icon"></span>
                                            <input class="form-control" type="text" placeholder="City, airport or address">
                                        </div>
                                    </div>
                                </div><!-- end col-lg-4 -->
                                <div class="col-lg-4 pr-0">
                                    <div class="input-box">
                                        <label class="label-text">Pick-up date</label>
                                        <div class="form-group">
                                            <span class="la la-calendar form-icon"></span>
                                            <input class="date-range form-control" type="text" name="daterange-single" readonly>
                                        </div>
                                    </div>
                                </div><!-- end col-lg-4 -->
                                <div class="col-lg-4">
                                    <div class="input-box">
                                        <label class="label-text">Time</label>
                                        <div class="form-group">
                                            <div class="select-contain w-auto">
                                                <select class="select-contain-select">
                                                    <option value="1200AM">12:00AM</option>
                                                    <option value="1230AM">12:30AM</option>
                                                    <option value="0100AM">1:00AM</option>
                                                    <option value="0130AM">1:30AM</option>
                                                    <option value="0200AM">2:00AM</option>
                                                    <option value="0230AM">2:30AM</option>
                                                    <option value="0300AM">3:00AM</option>
                                                    <option value="0330AM">3:30AM</option>
                                                    <option value="0400AM">4:00AM</option>
                                                    <option value="0430AM">4:30AM</option>
                                                    <option value="0500AM">5:00AM</option>
                                                    <option value="0530AM">5:30AM</option>
                                                    <option value="0600AM">6:00AM</option>
                                                    <option value="0630AM">6:30AM</option>
                                                    <option value="0700AM">7:00AM</option>
                                                    <option value="0730AM">7:30AM</option>
                                                    <option value="0800AM">8:00AM</option>
                                                    <option value="0830AM">8:30AM</option>
                                                    <option value="0900AM" selected>9:00AM</option>
                                                    <option value="0930AM">9:30AM</option>
                                                    <option value="1000AM">10:00AM</option>
                                                    <option value="1030AM">10:30AM</option>
                                                    <option value="1100AM">11:00AM</option>
                                                    <option value="1130AM">11:30AM</option>
                                                    <option value="1200PM">12:00PM</option>
                                                    <option value="1230PM">12:30PM</option>
                                                    <option value="0100PM">1:00PM</option>
                                                    <option value="0130PM">1:30PM</option>
                                                    <option value="0200PM">2:00PM</option>
                                                    <option value="0230PM">2:30PM</option>
                                                    <option value="0300PM">3:00PM</option>
                                                    <option value="0330PM">3:30PM</option>
                                                    <option value="0400PM">4:00PM</option>
                                                    <option value="0430PM">4:30PM</option>
                                                    <option value="0500PM">5:00PM</option>
                                                    <option value="0530PM">5:30PM</option>
                                                    <option value="0600PM">6:00PM</option>
                                                    <option value="0630PM">6:30PM</option>
                                                    <option value="0700PM">7:00PM</option>
                                                    <option value="0730PM">7:30PM</option>
                                                    <option value="0800PM">8:00PM</option>
                                                    <option value="0830PM">8:30PM</option>
                                                    <option value="0900PM">9:00PM</option>
                                                    <option value="0930PM">9:30PM</option>
                                                    <option value="1000PM">10:00PM</option>
                                                    <option value="1030PM">10:30PM</option>
                                                    <option value="1100PM">11:00PM</option>
                                                    <option value="1130PM">11:30PM</option>
                                                </select>
                                            </div>
                                        </div>
                                    </div>
                                </div><!-- end col-lg-4 -->
                            </form>
                            <form action="#" class="row align-items-center">
                                <div class="col-lg-4 pr-0">
                                    <div class="input-box">
                                        <label class="label-text">Drop-off</label>
                                        <div class="form-group">
                                            <span class="la la-map-marker form-icon"></span>
                                            <input class="form-control" type="text" placeholder="Same as pick-up">
                                        </div>
                                    </div>
                                </div><!-- end col-lg-4 -->
                                <div class="col-lg-4 pr-0">
                                    <div class="input-box">
                                        <label class="label-text">Drop-off date</label>
                                        <div class="form-group">
                                            <span class="la la-calendar form-icon"></span>
                                            <input class="date-range form-control" type="text" name="daterange-single" readonly>
                                        </div>
                                    </div>
                                </div><!-- end col-lg-4 -->
                                <div class="col-lg-4">
                                    <div class="input-box">
                                        <label class="label-text">Time</label>
                                        <div class="form-group">
                                            <div class="select-contain w-auto">
                                                <select class="select-contain-select">
                                                    <option value="1200AM">12:00AM</option>
                                                    <option value="1230AM">12:30AM</option>
                                                    <option value="0100AM">1:00AM</option>
                                                    <option value="0130AM">1:30AM</option>
                                                    <option value="0200AM">2:00AM</option>
                                                    <option value="0230AM">2:30AM</option>
                                                    <option value="0300AM">3:00AM</option>
                                                    <option value="0330AM">3:30AM</option>
                                                    <option value="0400AM">4:00AM</option>
                                                    <option value="0430AM">4:30AM</option>
                                                    <option value="0500AM">5:00AM</option>
                                                    <option value="0530AM">5:30AM</option>
                                                    <option value="0600AM">6:00AM</option>
                                                    <option value="0630AM">6:30AM</option>
                                                    <option value="0700AM">7:00AM</option>
                                                    <option value="0730AM">7:30AM</option>
                                                    <option value="0800AM">8:00AM</option>
                                                    <option value="0830AM">8:30AM</option>
                                                    <option value="0900AM" selected>9:00AM</option>
                                                    <option value="0930AM">9:30AM</option>
                                                    <option value="1000AM">10:00AM</option>
                                                    <option value="1030AM">10:30AM</option>
                                                    <option value="1100AM">11:00AM</option>
                                                    <option value="1130AM">11:30AM</option>
                                                    <option value="1200PM">12:00PM</option>
                                                    <option value="1230PM">12:30PM</option>
                                                    <option value="0100PM">1:00PM</option>
                                                    <option value="0130PM">1:30PM</option>
                                                    <option value="0200PM">2:00PM</option>
                                                    <option value="0230PM">2:30PM</option>
                                                    <option value="0300PM">3:00PM</option>
                                                    <option value="0330PM">3:30PM</option>
                                                    <option value="0400PM">4:00PM</option>
                                                    <option value="0430PM">4:30PM</option>
                                                    <option value="0500PM">5:00PM</option>
                                                    <option value="0530PM">5:30PM</option>
                                                    <option value="0600PM">6:00PM</option>
                                                    <option value="0630PM">6:30PM</option>
                                                    <option value="0700PM">7:00PM</option>
                                                    <option value="0730PM">7:30PM</option>
                                                    <option value="0800PM">8:00PM</option>
                                                    <option value="0830PM">8:30PM</option>
                                                    <option value="0900PM">9:00PM</option>
                                                    <option value="0930PM">9:30PM</option>
                                                    <option value="1000PM">10:00PM</option>
                                                    <option value="1030PM">10:30PM</option>
                                                    <option value="1100PM">11:00PM</option>
                                                    <option value="1130PM">11:30PM</option>
                                                </select>
                                            </div>
                                        </div>
                                    </div>
                                </div><!-- end col-lg-4 -->
                            </form>
                        </div>
                        <div class="advanced-wrap">
                            <a class="btn collapse-btn theme-btn-hover-gray font-size-15" data-toggle="collapse" href="#collapseSix" role="button" aria-expanded="false" aria-controls="collapseSix">
                                Advanced options <i class="la la-angle-down ml-1"></i>
                            </a>
                            <div class="pt-3 collapse" id="collapseSix">
                                <div class="row">
                                    <div class="col-lg-3 pr-0">
                                        <div class="input-box">
                                            <label class="label-text">Car type</label>
                                            <div class="form-group">
                                                <div class="select-contain w-auto">
                                                    <select class="select-contain-select">
                                                        <option value="1">No preference</option>
                                                        <option value="2">Economy</option>
                                                        <option value="3">Compact</option>
                                                        <option value="4">Midsize</option>
                                                        <option value="5">Standard</option>
                                                        <option value="6">Fullsize</option>
                                                        <option value="7">Premium</option>
                                                        <option value="8">Luxury</option>
                                                        <option value="9">Convertible</option>
                                                        <option value="10">Minivan</option>
                                                        <option value="11">Sport Utility</option>
                                                        <option value="12">Sports car</option>
                                                    </select>
                                                </div>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-3 -->
                                    <div class="col-lg-3 pr-0">
                                        <div class="input-box">
                                            <label class="label-text">Rental car company</label>
                                            <div class="form-group">
                                                <div class="select-contain w-auto">
                                                    <select class="select-contain-select">
                                                        <option value="">No preference</option>
                                                        <option value="AC">ACE Rent A Car</option>
                                                        <option value="AD">Advantage Rent-A-Car</option>
                                                        <option value="AL">Alamo Rent A Car</option>
                                                        <option value="ZI">Avis</option>
                                                        <option value="ZD">Budget</option>
                                                        <option value="ZR">Dollar Rent A Car</option>
                                                        <option value="EY">Economy Rent a Car</option>
                                                        <option value="ET">Enterprise</option>
                                                        <option value="EP">Europcar</option>
                                                        <option value="FX">Fox Rental Cars</option>
                                                        <option value="ZE">Hertz</option>
                                                        <option value="MW">Midway Car Rental</option>
                                                        <option value="ZL">National Car Rental</option>
                                                        <option value="NU">Nü Car</option>
                                                        <option value="ZA">Payless</option>
                                                        <option value="RO">Routes Car Rental</option>
                                                        <option value="SX">Sixt</option>
                                                        <option value="ZT">Thrifty Car Rental</option>
                                                        <option value="SV">U-Save</option>
                                                        <option value="SC">Silvercar</option>
                                                    </select>
                                                </div>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-3 -->
                                    <div class="col-lg-3">
                                        <div class="input-box">
                                            <label class="label-text">Discount code</label>
                                            <div class="form-group">
                                                <div class="select-contain w-auto">
                                                    <select class="select-contain-select">
                                                        <option value="0">I don't have a code</option>
                                                        <option value="1">Corporate or contracted</option>
                                                        <option value="2">Special or advertised</option>
                                                    </select>
                                                </div>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-3 -->
                                </div><!-- end row -->
                            </div>
                        </div><!-- end advanced-wrap -->
                        <div class="btn-box pt-3">
                            <input type="submit" class="theme-btn" value="Search" />
                            <!-- end row -->
                        </div>                        
                    </div>
                    <div class="tab-pane fade" id="cruise" role="tabpanel" aria-labelledby="cruise-tab">
                                
                        <div class="contact-form-action">
                            <form action="search_cruises.php" method="post" class="row align-items-center">
                                <div class="col-lg-3 pr-0">
                                    <div class="input-box">
                                        <label class="label-text">Going to</label>
                                        <div class="form-group">
                                            <div class="select-contain w-auto">
                                                <select class="select-contain-select">
                                                    <option value="">Select destination</option>
                                                    <optgroup label="Most Popular">
                                                        <option value="caribbean">Caribbean</option>
                                                        <option value="bahamas">Bahamas</option>
                                                        <option value="mexico">Mexico</option>
                                                        <option value="alaska">Alaska</option>
                                                        <option value="europe">Europe</option>
                                                        <option value="bermuda">Bermuda</option>
                                                        <option value="hawaii">Hawaii</option>
                                                        <option value="nepal">Nepal</option>
                                                        <option value="italy">Italy</option>
                                                        <option value="canada-new-england">Canada / New England</option>
                                                    </optgroup>
                                                    <optgroup label="Other Destinations">
                                                        <option value="arctic-antarctic">Arctic / Antarctic</option>
                                                        <option value="middle-east">Middle East</option>
                                                        <option value="africa">Africa</option>
                                                        <option value="panama-canal">Panama Canal</option>
                                                        <option value="asia">Asia</option>
                                                        <option value="pacific-coastal">Pacific Coastal</option>
                                                        <option value="australia-new-zealand">Australia / New Zealand</option>
                                                        <option value="central-america">Central America</option>
                                                        <option value="galapagos">Galapagos</option>
                                                        <option value="getaway-at-sea">Getaway at Sea</option>
                                                        <option value="transatlantic">Transatlantic</option>
                                                        <option value="world-cruise">World</option>
                                                        <option value="south-america">South America</option>
                                                        <option value="south-pacific">South Pacific</option>
                                                        <option value="transpacific">Transpacific</option>
                                                    </optgroup>
                                                </select>
                                            </div>
                                        </div>
                                    </div>
                                </div><!-- end col-lg-3 -->
                                <div class="col-lg-3 pr-0">
                                    <div class="input-box">
                                        <label class="label-text">Departs as early as</label>
                                        <div class="form-group">
                                            <span class="la la-calendar form-icon"></span>
                                            <input class="date-range form-control" type="text" name="daterange-single" readonly>
                                        </div>
                                    </div>
                                </div><!-- end col-lg-3 -->
                                <div class="col-lg-3 pr-0">
                                    <div class="input-box">
                                        <label class="label-text">Departs as late as</label>
                                        <div class="form-group">
                                            <span class="la la-calendar form-icon"></span>
                                            <input class="date-range form-control" type="text" name="daterange-single" readonly>
                                        </div>
                                    </div>
                                </div><!-- end col-lg-3 -->
                                <div class="col-lg-3">
                                    <div class="input-box">
                                        <label class="label-text">Travelers in the cabin</label>
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
                                                                <input type="text" name="adult_number" value="0">
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
                                </div><!-- end col-lg-3 -->
                                </form>
                        </div>
                        <div class="btn-box">
                            <input type="submit" class="theme-btn" value="Search" />
                            
                        </div>                        
                    </div>
                    <div class="tab-pane fade" id="tour" role="tabpanel" aria-labelledby="tour-tab">
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
                        </div>                       
                    </div>
                    <div class="tab-pane fade" id="visa" role="tabpanel" aria-labelledby="visa-tab">
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
                    </div>
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
                            <a href="index.html" class="foot__logo"><img src="/assets/images/logo.png" alt="logo"></a>
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
    <div class="modal-popup">
        <div class="modal fade" id="signupPopupForm" tabindex="-1" role="dialog"  aria-hidden="true">
            <div class="modal-dialog modal-dialog-centered" role="document">
                <div class="modal-content">
                    <div class="modal-header">
                        <div>
                            <h5 class="modal-title title" id="exampleModalLongTitle">Sign Up</h5>
                            <p class="font-size-14">Hello! Welcome Create a New Account</p>
                        </div>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true" class="la la-close"></span>
                        </button>
                    </div>
                    <div class="modal-body">
                        <div class="contact-form-action">
                            <form method="post">
                                <div class="input-box">
                                    <label class="label-text">Full Name</label>
                                    <div class="form-group">
                                        <span class="la la-user form-icon"></span>
                                        <input class="form-control" type="text" name="text" placeholder="Type your username">
                                    </div>
                                </div><!-- end input-box -->
                                <div class="input-box">
                                    <label class="label-text">Email Address</label>
                                    <div class="form-group">
                                        <span class="la la-envelope form-icon"></span>
                                        <input class="form-control" type="text" name="text" placeholder="Type your email">
                                    </div>
                                </div><!-- end input-box -->
                                <div class="input-box">
                                    <label class="label-text">Password</label>
                                    <div class="form-group">
                                        <span class="la la-lock form-icon"></span>
                                        <input class="form-control" type="text" name="text" placeholder="Type password">
                                    </div>
                                </div><!-- end input-box -->
                                <div class="input-box">
                                    <label class="label-text">Repeat Password</label>
                                    <div class="form-group">
                                        <span class="la la-lock form-icon"></span>
                                        <input class="form-control" type="text" name="text" placeholder="Type again password">
                                    </div>
                                </div><!-- end input-box -->
                                <div class="btn-box pt-3 pb-4">
                                    <button type="button" class="theme-btn w-100">Register Account</button>
                                </div>
                                
                            </form>
                        </div><!-- end contact-form-action -->
                    </div>
                </div>
            </div>
        </div>
    </div><!-- end modal-popup -->

    <!-- end modal-shared -->
    <div class="modal-popup">
        <div class="modal fade" id="loginPopupForm" tabindex="-1" role="dialog"  aria-hidden="true">
            <div class="modal-dialog modal-dialog-centered" role="document">
                <div class="modal-content">
                    <div class="modal-header">
                        <div>
                            <h5 class="modal-title title" id="exampleModalLongTitle2">Login</h5>
                            <p class="font-size-14">Hello! Welcome to your account</p>
                        </div>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true" class="la la-close"></span>
                        </button>
                    </div>
                    <div class="modal-body">
                        <div class="contact-form-action">
                            <form method="post">
                                <div class="input-box">
                                    <label class="label-text">Username</label>
                                    <div class="form-group">
                                        <span class="la la-user form-icon"></span>
                                        <input class="form-control" type="text" name="text" placeholder="Type your username">
                                    </div>
                                </div><!-- end input-box -->
                                <div class="input-box">
                                    <label class="label-text">Password</label>
                                    <div class="form-group mb-2">
                                        <span class="la la-lock form-icon"></span>
                                        <input class="form-control" type="text" name="text" placeholder="Type your password">
                                    </div>
                                    <div class="d-flex align-items-center justify-content-between">
                                        <p class="forgot-password">
                                            <a href="recover.html">Forgot Password?</a>
                                        </p>
                                    </div>
                                </div><!-- end input-box -->
                                <div class="btn-box pt-3 pb-4">
                                    <button type="button" class="theme-btn w-100">Login Account</button>
                                </div>
                            </form>
                        </div><!-- end contact-form-action -->
                    </div>
                </div>
            </div>
        </div>
    </div><!-- end modal-popup -->
</template>
