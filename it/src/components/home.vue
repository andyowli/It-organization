<template>
    <div>
        <!-- Head -->
        <header class="header" data-header>
            <div class="container">
                <a href="#" class="logo">
                    <img src="../../static/images/logo.svg" alt="Solutry logo">
                </a>
                <!-- <button class="nav-toggle-btn" data-nav-toggle-btn>
                    <ion-icon name="menu-outline" class="open"></ion-icon>
                    <ion-icon name="close-outline" class="close"></ion-icon>
                </button> -->
                <nav class="navbar">
                    <div class="container">
                    <ul class="navbar-list">

                        <li>
                        <a href="#home" class="navbar-link" data-navbar-link>Home</a>
                        </li>

                        <li>
                        <a href="#features" class="navbar-link" data-navbar-link>Features</a>
                        </li>

                        <li>
                        <a href="#service" class="navbar-link" data-navbar-link>Service</a>
                        </li>

                        <li>
                        <a href="#blog" class="navbar-link" data-navbar-link>Blog</a>
                        </li>

                        <li>
                        <a href="#newsletter" class="navbar-link" data-navbar-link>Newsletter</a>
                        </li>
                    </ul>
                    </div>
                </nav>
                <button class="btn btn-secondary">
                    <span>Get Started</span>  
                </button>
            </div>
        </header>

        <main>
            <article>
                <!-- Home -->
                <section class="hero" id="home">
                    <img src="../../static/images/shape1.png" alt="Illustration art" class="shape shape-1">
                    <img src="../../static/images/shape2.png" alt="Illustration art" class="shape shape-2">
                    <img src="../../static/images/shape3.png" alt="Illustration art" class="shape shape-3">
                    <div class="container" v-for="(hero,home) in index" :key="home">
                        <figure class="hero-banner">
                            <img :src="hero.image" alt="Illustration art" loading="lazy" class="w-100">
                        </figure>
                        <div class="hero-content">
                            <h2 class="h1 hero-title">{{hero.title}}</h2>
                            <p class="section-text">
                               {{hero.text}}
                            </p>
                            <button class="btn btn-primary">
                                <span>{{hero.btnMsg}}</span>
                            </button>
                        </div>
                    </div>
                </section>

                <!-- Features -->

                <section class="features" id="features">
                    <div class="container">
                        <p class="section-subtitle">How Can Help You</p>
                        <h2 class="h2 section-title">We're helping teams do their best work</h2>
                        <ul class="features-list">
                            <li v-for="(item,index) in features" :key="index">
                                <div class="features-card">
                                    <div class="card-icon">
                                        <img :src="item.image" alt="Illustration icon">
                                    </div>
                                    <h3 class="h3 card-title">{{item.title}}</h3>
                                    <p class="card-text">
                                        {{item.content}}
                                    </p>
                                    <a href="#" class="card-link">
                                        <span>{{item.chank}}</span>
                                        <ion-icon name="chevron-forward-outline"></ion-icon>
                                    </a>
                                </div>
                            </li>
                        </ul>
                    </div>
                </section>

                <!-- Service -->
                <section class="service" id="service">
                    <div class="container">
                        <figure class="service-banner">
                            <img src="../../static/images/service-1.png" alt="Illustration art" loading="lazy" class="w-100">
                        </figure>
                        <div class="service-content">
                            <p class="section-subtitle">Services We Offer</p>
                            <h2 class="h2 section-title">We are here, to help your startup business</h2>
                            <ul class="service-list">
                                <li class="service-item" v-for="(type,typeNum) in serMesg" :key="typeNum">
                                    <div class="service-item-icon">
                                        <!-- <ion-icon name="checkmark-outline"></ion-icon> -->
                                        <span class="iconfont icon-duihao"></span>
                                    </div>
                                    <h3 class="h3 service-item-title">{{type.typeTitle}}</h3>
                                </li>
                            </ul>
                        </div>

                        <figure class="service-banner">
                            <img src="../../static/images/service-2.png" alt="Illustration art" loading="lazy" class="w-100">
                        </figure>

                        <div class="service-content">
                            <p class="section-subtitle">Our Services</p>
                            <h2 class="h2 section-title">Best IT & technology service in your area</h2>
                            <ul class="service-list">
                                <li class="service-item" v-for="(Development,type) in service " :key="type">
                                    <div class="service-item-icon">
                                        <span class="iconfont icon-duihao"></span>
                                    </div>
                                    <h3 class="h3 service-item-title">{{Development.dTit}}</h3>
                                </li>
                            </ul>
                        </div>
                    </div>
                </section>

                <!-- 
                    - #BLOG
                -->
                <section class="blog" id="blog">
                    <div class="container">
                        <p class="section-subtitle">Latest News</p>
                        <h2 class="h2 section-title">Our latest articles & resources</h2>
                        <ul class="blog-list">
                            <li v-for="(a,b) in newsMessage" :key="b">
                                <div class="blog-card">
                                    <figure class="blog-banner">
                                        <a href="#">
                                            <img :src="a.image" alt="How is technology working with new things?"
                                            loading="lazy" class="w-100">
                                        </a>
                                    </figure>

                                    <div class="blog-content">
                                        <ul class="blog-meta-list">
                                            <li class="blog-meta-item">
                                                <!-- <ion-icon name="pricetag-outline"></ion-icon> -->
                                                <a href="#" class="blog-meta-link">{{a.newType}}</a>
                                            </li>
                                            <li class="blog-meta-item">
                                                <ion-icon name="calendar-number-outline"></ion-icon>
                                                <time class="blog-meta-time" datetime="2022-02-25">{{a.time}}</time>
                                            </li>
                                        </ul>
                                        <h3 class="h3 blog-title">
                                            <a href="#">{{a.newTitle}}</a>
                                        </h3>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </section>

                <!-- 
                    - #NEWSLETTER
                -->
                <section class="newsletter" id="newsletter">
                    <div class="container">
                        <figure class="newsletter-banner">
                            <img src="../../static/images/newsletter.png" alt="Illustration art" loading="lazy" class="w-100">
                        </figure>
                        <div class="newsletter-content">
                            <p class="section-subtitle">Subscribe Our Newsletter</p>
                            <h2 class="h2 section-title">The latest resources, sent to your inbox weekly</h2>
                            <form action="" class="newsletter-form">
                                <input type="email" name="email" required placeholder="Enter your email address" class="input-field">
                                <button type="submit" class="btn btn-primary">
                                    <span>Subscribe Now</span>
                                    <ion-icon name="chevron-forward-outline"></ion-icon>
                                </button>
                            </form>

                        </div>
                    </div>
                </section>
            </article>
        </main>

        <!-- 
            - #FOOTER
        -->
        <footer class="footer">
            <div class="footer-top">
                <div class="container">
                    <div class="footer-brand">
                        <a href="#" class="logo">
                            <img src="../../static/images/logo.svg" alt="Solutry logo">
                        </a>
                        <p class="section-text">
                            Lorem ipsum dolor sit amet, consectetur, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
                            minim.
                        </p>
                        <div class="location-text">
                            <div class="location-icon">
                                <span class="iconfont icon-ditu_dingwei_o"></span>
                            </div>

                            <address class="address">
                                Tianfu 4th Street, Chengdu, China
                            </address>
                        </div>
                    </div>
                    <div class="quicklink-box">
                        <p class="h3 quicklink-title">Quick links</p>
                        <ul class="quicklink-list">
                            <li v-for="(link,linkIndex) in footList" :key="linkIndex">
                                <a href="#" class="quicklink">{{link.jump}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="contact">
                        <p class="h3 contact-title">Contact with us</p>
                        <ul class="contact-list">
                            <li class="contact-item">
                                <div class="contact-icon">
                                    <span class="iconfont icon-xinxi"></span>
                                </div>
                                <a href="mailto:kissfish1376@163.com" class="contact-link">kissfish1376@163.com</a>
                            </li>
                            <li class="contact-item">
                                <div class="contact-icon">
                                    <span class="iconfont icon-dianhua"></span>
                                </div>
                                <a href="tel:+14854560102" class="contact-link">+1-485-456-0102</a>
                            </li>

                        </ul>
                    </div>
                </div>
            </div>

            <div class="footer-bottom">
                <div class="container">
                    <p class="copyright">
                        &copy; 2022 <a href="#">codewithsadee</a>. All Rights Reserved
                    </p>
                    <ul class="social-list">
                        <li>
                            <a href="#" class="social-link">
                                <span class="iconfont icon-facebook"></span>
                            </a>
                        </li>
                        <li>
                            <a href="#" class="social-link">
                                <span class="iconfont icon-twitter-line"></span>
                            </a>
                        </li>
                        <li>
                            <a href="#" class="social-link">
                                <span class="iconfont icon-sociallinkedinoutline"></span>
                            </a>
                        </li>
                        <li>
                            <a href="#" class="social-link">
                                <span class="iconfont icon-instagram"></span>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </footer>
    </div>
</template>

<!-- <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
<script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script> -->
<script>
export default {
    data(){
        return {
            index:[
                {
                    image:require('../../static/images/hero-banner.png'),
                    title:'Secure IT solutions for a more secure environment',
                    text:' Velit hendrerit sit auctor tempor sem. Congue mi tempor condimentum felis arcu, non cursus. Nulla pharetra porttitor sed platea arcu et leo odio.',
                    btnMsg:'Get Started Now'
                }
            ],
            features:[
                {
                    title:'Zero Configuration',
                    content:'Lorem ipsum dolor sit amet, conse ctetur adipiscing elit. Sed est non feugiat sagittis.',
                    chank:'Learn More',
                    image:require('../../static/images/features-icon-1.png')
                },
                {
                    title:'Code Security',
                    content:'Lorem ipsum dolor sit amet, conse ctetur adipiscing elit. Sed est non feugiat sagittis.',
                    chank:'Learn More',
                    image:require('../../static/images/features-icon-2.png')
                },
                {
                    title:'Team Management',
                    content:'Lorem ipsum dolor sit amet, conse ctetur adipiscing elit. Sed est non feugiat sagittis.',
                    chank:'Learn More',
                    image:require('../../static/images/features-icon-3.png')
                },
                {
                    title:'Access Controlled',
                    content:'Lorem ipsum dolor sit amet, conse ctetur adipiscing elit. Sed est non feugiat sagittis.',
                    chank:'Learn More',
                    image:require('../../static/images/features-icon-4.png')
                }
            ],
            serMesg:[
                {typeTitle:'Cloud Databases'},
                {typeTitle:'Website Hosting'},
                {typeTitle:'Remote Desktop'},
                {typeTitle:'File Backup'},
            ],
            service:[
                {dTit:'Design & Development'},
                {dTit:'Mobile Apps Development'},
                {dTit:'Laravel Web Development'},
                {dTit:'Vue Web Development'},
            ],
            newsMessage:[
                {
                    image:require('../../static/images/blog-1.jpg'),
                    newType:'Design',
                    time:'25 FEB, 2022',
                    newTitle:'How can design make products better reflect?'
                },
                {
                    image:require('../../static/images/blog-2.jpg'),
                    newType:'Mobile',
                    time:'25 FEB, 2022',
                    newTitle:'Development of Internet mobile applications'
                },
                {
                    image:require('../../static/images/blog-3.jpg'),
                    newType:'STARTUP',
                    time:'25 FEB, 2022',
                    newTitle:'How to help the project landing?'
                }
            ],
            footList:[
                {jump:'IT Startup'},
                {jump:'Software'},
                {jump:'Business'},
                {jump:'App'},
                {jump:'Insurance'},
                {jump:'Property'},
                {jump:'Big Data'},
                {jump:'Distance Learning'},
                {jump:'Chatbot'},
                {jump:'Medical'},
            ]
        }
    }
}
</script>

<style scoped>
@import '../../static/css/style.css';
@import '../../static/css/icon/iconfont.css';
</style>