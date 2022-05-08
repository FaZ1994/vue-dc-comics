<template>
   <section class="footerTop">
        <img src="../assets/img/dc-logo-bg.png" alt="">
        <div class="footerTopContainer">
            <ul>
                <li class="title">Dc comics</li>
                <li v-for="(item, index) in links" :key="index">{{item.text}}</li>
            </ul>
            <ul>
                <li class="title">Shop</li>
                <li v-for="(item, index) in shopLinks" :key="index">{{item.text}}</li>
            </ul>
            <ul>
                <li class="title">Dc</li>
                <li v-for="(item, index) in dcLinks" :key="index">{{item.text}}</li>
            </ul>
            <ul>
                <li class="title">Sites</li>
                <li v-for="(item, index) in sitesLinks" :key="index">{{item.text}}</li>
            </ul>
        </div>
    </section>
</template>




<script>
export default {
    name: 'AppFooterTop',
    data(){
        return{
            links:[
                {
                    text: "Characters",
                    link: ""
                },
                {
                    text: "Comics",
                    link: ""
                },
                {
                    text: "Movies",
                    link: ""
                },
                {
                    text: "TV",
                    link: ""
                },
                {
                    text: "Games",
                    link: ""
                },
                {
                    text: "Videos",
                    link: ""
                },
                {
                    text: "News",
                    link: ""
                },
            ],
            shopLinks:[
                {
                    text: "Shop DC",
                    link: ""
                },
                {
                    text: "Shop DC Collectibles",
                    link: ""
                }
            ],
            dcLinks:[
                {
                    text: "Terms Of use",
                    link: ""
                },
                {
                    text: "Privacy policy (New)",
                    link: ""
                },
                {
                    text: "Ad Choices",
                    link: ""
                },
                {
                    text: "Advertising",
                    link: ""
                },
                {
                    text: "Jobs",
                    link: ""
                },
                {
                    text: "Subscriptions",
                    link: ""
                },
                {
                    text: "Talent Workshops",
                    link: ""
                },
                {
                    text: "CPSC Certificates",
                    link: ""
                },
                {
                    text: "Ratings",
                    link: ""
                },
                {
                    text: "Shop Help",
                    link: ""
                },
                {
                    text: "Contact Us",
                    link: ""
                },
            ],
            sitesLinks:[
                {
                    text: "DC",
                    link: ""
                },
                {
                    text: "MAD Magazine",
                    link: ""
                },
                {
                    text: "DC Kids",
                    link: ""
                },
                {
                    text: "DC Universe",
                    link: ""
                },
                {
                    text: "DC Power Visa",
                    link: ""
                },
            ],
        }
    },
    props: {
        msg: String
    }
}
</script>

<style scoped lang="scss">

@import './style/generals';
@import './style/vars';

.footerTop {
    background-image: url("../assets/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    overflow: hidden;
    position: relative;
    img {
        position: absolute;
        right: 0%;
        top: 50%;
        transform: translate(-50%, -50%);
        height: 540px;
        z-index: 0;
    }
}
.footerTopContainer {
    width: 70%;
    height: 60vh;
    margin: 0 auto;
    padding: 50px 0;
    display: flex;
    flex-flow: column wrap;
    align-content: flex-start;
    gap: 2em;
    ul {
        list-style: none;
        li {
            color: $fontNav;

        }
        .title {
            color: $fontMain;
            text-transform: uppercase;
            padding: 10px 0;
        }
    }
}
</style>