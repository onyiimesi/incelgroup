<script setup>

</script>

<template>
    <!-- ================================
    START HERO-WRAPPER AREA
    ================================= -->
    <section class="hero-wrapper hero-wrapper6">
        <div class="hero-box hero-bg-6" style="background-image: url(/assets/images/banner_hotel.jpg)">
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
