<template>
    <div>
        <HeaderBanner 
            banner-title="WELCOME TO KBS HEALTH CARE"
            banner-text="We provide Medical Billing, Coding & Audits, AR, Denial Management, RCM Solutions, Credit Balance Resolution, Eligibility and Verifications and numerous more services to Dentists, Clinics and Hospitals, helping them concentrate on their core." 
            :banner-image='bannerImage'>
        </HeaderBanner>

        <!-- <div class="container" style="margin-top: -60px;margin-bottom: 60px;">
        <div class="row">
        <div class="col-md-4  aos-animate" data-aos="fade-up" data-aos-duration="1000" data-aos-once="true">
        <div class="media block-icon-1 d-block text-left">
        <div class="icon mb-3">
        <img
        src="../assets/flaticon/svg/001-consultation.svg"
        alt="Image"
        class="img-fluid"
        />
        </div>
        <div class="media-body">
        <h3 class="h5 mb-4">Corporate Collaboration</h3>
        <p>
        A small river named Duden flows by their place and supplies it
        with the necessary regelialia.
        </p>
        <p> <router-link to="/about-us" class="btn btn-primary"> Learn More </router-link></p>
        </div>
        </div>

        </div>
        <div class="col-md-4  aos-animate" data-aos="fade-up" data-aos-duration="1000" data-aos-once="true">
        <div class="media block-icon-1 d-block text-left">
        <div class="icon mb-3">
        <img
        src="../assets/flaticon/svg/002-discussion.svg"
        alt="Image"
        class="img-fluid"
        />
        </div>
        <div class="media-body">
        <h3 class="h5 mb-4">Strategic Partners</h3>
        <p>
        A small river named Duden flows by their place and supplies it
        with the necessary regelialia.
        </p>
        <p> <router-link to="/about-us" class="btn btn-primary"> Learn More </router-link></p>
        </div>
        </div>
        </div>
        <div class="col-md-4  aos-animate" data-aos="fade-up" data-aos-duration="1000" data-aos-once="true">
        <div class="media block-icon-1 d-block text-left">
        <div class="icon mb-3">
        <img
        src="../assets/flaticon/svg/003-turnover.svg"
        alt="Image"
        class="img-fluid"
        />
        </div>
        <div class="media-body">
        <h3 class="h5 mb-4">Infinite Posibilities</h3>
        <p>
        A small river named Duden flows by their place and supplies it
        with the necessary regelialia.
        </p>
        <p> <router-link to="/about-us" class="btn btn-primary"> Learn More </router-link></p>
        </div>
        </div>
        </div>
        </div>
        </div> -->
        <!-- About us -->
        <div class="about-banner">    
            <div class="container">
                <div class="row pt-5 pb-5">
                    <div class="col-sm-12" style="background: #4444449c">
                        <h2 class="pb-3 pt-4 text-center text-uppercase text-white">About Us</h2>
                        <p data-aos="slide-up" data-aos-easing="ease" data-aos-duration="1000" data-aos-once="true" class="text-white">
                            At core, KBS dedicates itself towards delivering services and solutions that meet the expectations of our Clients. At KBS we understand that each Customer has specific needs and requirements. Hence, we provide customized solutions to our Clients to suit their needs. Over the last 5 years, since inception in 2015, KBS has provided services to large and small organizations who have entrusted in us their full faith owing to the broad-base approach leadership and unrivalled client support. KBS is, after all, about people.

                            <!-- KBS dedication to delivering solutions that meet and exceed, the needs of customers has been driven since KBS was formed in 2015. Over 5 years, large and small organizations have put their trust in us – in our broad-based approaches, leadership and unrivalled client support. Working every day and developing new ways for our customers to have a positive impact. Because KBS is, after all, about people. -->
                        </p>
                        <p> 
                            <router-link to="/about-us" class="btn btn-primary"> Learn More </router-link>
                        </p>
                    </div>
                    <div class="col-sm-4"></div>
                </div>
            </div>
        </div>

        <!-- our services -->
        <div class="container">
            <div class="row">
                <div class="col-12 text-center mb-3 mt-5">
                    <h2>OUR SERVICE EXPERTISE</h2>
                </div>
                <div v-for="service in listServices" :key="service.name" class="col-md-4 mb-5  aos-animate" data-aos="fade-up">
                    <div class="media block-icon-1 d-block text-center">
                        <div class="icon mb-3">
                            <img :src="service.icon" alt="Image" class="img-fluid" />
                        </div>
                        <div class="media-body">
                            <h3 class="h5 mb-4">{{ service.name }}</h3>
                            <p>{{ service.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row pb-5">
                <div class="col-md-12 text-center  aos-animate" data-aos="fade-up" data-aos-duration="1000" data-aos-once="true">
                    <router-link to="/service" class="btn btn-primary py-3 px-4"> MORE SERVICE FEATURES </router-link>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import consultationSvg from "../assets/images/flaticon/svg/001-consultation.svg";
    import discussionSvg from "../assets/images/flaticon/svg/002-discussion.svg";
    import gear from "../assets/images/flaticon/svg/004-gear.svg";
    import conflict from "../assets/images/flaticon/svg/005-conflict.svg";
    import turnoverSvg from "../assets/images/flaticon/svg/003-turnover.svg";
    import meeting from "../assets/images/flaticon/svg/006-meeting.svg";
    import brainstorming from "../assets/images/flaticon/svg/007-brainstorming.svg";

    // import HappyCustomersQuotes from '../views/HappyCutomersQuotes' ;
    import HeaderBanner from '../views/HeaderBanner';

    import bannerImage  from  '../assets/homebanner1.png';
    export default {
        components: {
            // HappyCustomersQuotes,
            HeaderBanner
        },
        data() {
            return {
                bannerImage,
                listServices: [
                    {
                        name: "Medical Billing",
                        description: "We specialize in providing medical billing solutions across specialties. Right from Charge Capture to Denials, we handle it all!",
                        icon: gear,
                    },
                    {
                        name: "Medical Coding & Audits",
                        description: "We have certified medical coding experts across specialties including Home Health & Hospice, Radiology, Pathology, etc.",
                        icon: conflict,
                    },
                    {
                        name: "Accounts Receivable",
                        description: "We help our clients to improve cash-flow and reduce days in A/R so that they get paid more, faster and at a much lower cost.",
                        icon: meeting,
                    },
                    {
                        name: "Denial Management",
                        description: "Our highly experienced team of billing professionals are quick, analytical problem solvers of rejected or denied claims.",
                        icon: brainstorming,
                    },
                    {
                        name: "End-to-End RCM Solutions",
                        description: "KBS  provides end-to-end, comprehensive Revenue Cycle Management solutions from payor credentialing to complete billing and collections services.",
                        icon: consultationSvg,
                    },
                    {
                        name: "Credit Balance Resolution",
                        description: "This liability carries with it real and serious financial and compliance risk. It is your fiduciary responsibility to manage these real risks.",
                        icon: discussionSvg,
                    },
                    {
                        name: "IT consulting",
                        description: "IT consulting services are advisory services that help clients assess different technology strategies and, in doing so, align their technology strategies with their business or process strategies.",
                        icon: turnoverSvg,
                    },
                ],
            };
        },
    };
</script>

<style scoped>
    .fade-enter-active {
        transition: opacity 0.25s ease-out;
    }
    .fade-enter {
        opacity: 0 !important;
    }
    /* about */
    .blu-bx {
        position: relative;
        z-index: 99;
        top: -77px;
        background: var(--clr-primary);
        opacity: 0.8;
        padding: 10px 50px;
        color: var(--clr-light);
        text-align: center;
        border-radius: 10px;
    } /* about */
    /* services */
    .gap {
        padding-bottom: 50px;
        padding-top: 35px;
    }
    .bor-bx {
        border: 1px dotted #ccc;
        padding: 2%;
        margin-top: 20px;
        background: var(--clr-grey);
        opacity: 0.8;
        border-radius: 10px;
    }
    .serv-tlts {
        text-align: center;
        color: var(--clr-light);
        display: block;
        margin: 0 auto 30px auto;
        width: 60%;
        padding-top: 10px !important;
        padding-bottom: 10px !important;
        background-color: var(--clr-primary) !important;
        font-size: var(--fs-h3);
    }
    .ngt-mrg {
        margin-top: -45px;
    }
    /* services */
    .block-icon-1 {
        z-index: 1;
        padding: 30px;
        background: #fff;
        -webkit-box-shadow: 0 15px 30px 0px rgba(0, 0, 0, 0.1);
        box-shadow: 0 15px 30px 0px rgba(0, 0, 0, 0.1);
        /* margin-top: -80px;
        margin-bottom: 80px; */
    }
    .block-icon-1 img {
        width: 70px;
    }
    .img-fluid {
        max-width: 100%;
        height: auto;
    }
    .block-icon-1 .icon {
        font-size: 40px;
    }
    .about-banner {
        /* background-image: url("../assets/abouts-banner.png"); */
        background-repeat: no-repeat;
        background-size: cover;
    }
</style>