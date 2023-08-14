<template>
		<nav class="nav">
        <i class="uil uil-bars navOpenBtn" @click="navOpen"></i>
        <a href="#" class="logo">Driving School</a>

        <ul class="nav-links">
            <i class="uil uil-times navCloseBtn" @click="navClose"></i>
            <li><a @click="goTop" style="cursor: pointer">Home</a></li>
            <li><a @click="goEngagement" style="cursor: pointer">Engagements</a></li>
            <li><a @click="goVehicles" style="cursor: pointer">Vehicles</a></li>
            <li><a @click="goTestimonials" style="cursor: pointer">Testimonials</a></li>
            <li><a @click="goAbout" style="cursor: pointer">About Us</a></li>
            <li><a @click="goContact" style="cursor: pointer">Contact Us</a></li>
        </ul>



    </nav>
</template>

<script>

export default {
    name: "NavBar",
	methods: {
        searchBox() {
            const nav = document.querySelector('.nav');
            const searchIcon = document.querySelector("#searchIcon");
            nav.classList.toggle("openSearch");
            nav.classList.remove("openNav");
            if (nav.classList.contains("openSearch")) {
                return searchIcon.classList.replace("uil-search", "uil-times");
            }
            searchIcon.classList.replace("uil-times", "uil-search");
		},
        navOpen() {
            const nav = document.querySelector('.nav');
            const navOpenBtn = document.querySelector('.navOpenBtn');
            const searchIcon = document.querySelector("#searchIcon");
            nav.classList.add('openNav');
            nav.classList.remove('openSearch');
            searchIcon.classList.replace("uil-times", 'uil-search')
		},
		navClose() {
            const nav = document.querySelector('.nav');
            nav.classList.remove('openNav');
		},
		goTop() {
            const section = document.getElementById('top-page');
            window.scrollTo({
				top: section.offsetTop,
				behavior: 'smooth'
			});
		},
        goVehicles() {
            const section = document.getElementById('our-vehicles');
            window.scrollTo({
				top: section.offsetTop,
				behavior: 'smooth'
			});
		},
        goEngagement() {
            const section = document.getElementById('go-engagements');
            window.scrollTo({
                top: section.offsetTop,
                behavior: 'smooth'
            });
        },
        goTestimonials() {
            const section = document.getElementById('go-avis');
            window.scrollTo({
                top: section.offsetTop,
                behavior: 'smooth'
            });
        },
        goAbout() {
            const section = document.getElementById('go-about');
            window.scrollTo({
                top: section.offsetTop,
                behavior: 'smooth'
            });
        },
        goContact() {
            const section = document.getElementById('go-contact');
            window.scrollTo({
                top: section.offsetTop,
                behavior: 'smooth'
            });
        }
	}
}
</script>

<style scoped>
.nav {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 15px 200px;
    background: #11101d;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}
.nav,
.nav .nav-links {
    display: flex;
    align-items: center;
}
.nav {
    justify-content: space-between;
}
a {
    color: #ececec;
    text-decoration: none;
}
.nav .logo {
    font-size: 22px;
    font-weight: 500;
}
.nav .nav-links {
    column-gap: 20px;
    list-style: none;
}
.nav .nav-links a {
    transition: all 0.2s linear;
}
.nav.openSearch .nav-links a {
    opacity: 0;
    pointer-events: none;
}
.nav .search-icon {
    color: #ececec;
    font-size: 20px;
    cursor: pointer;
}
.nav .search-box {
    position: absolute;
    right: 250px;
    height: 45px;
    max-width: 555px;
    width: 100%;
    opacity: 0;
    pointer-events: none;
    transition: all 0.2s linear;
}
.nav.openSearch .search-box {
    opacity: 1;
    pointer-events: auto;
}
.search-box .search-icon {
    position: absolute;
    left: 15px;
    top: 50%;
    color: #11101d;
    transform: translateY(-50%);
}
.search-box input {
    height: 100%;
    width: 100%;
    border: none;
    outline: none;
    border-radius: 6px;
    background-color: #ececec;
    padding: 0 15px 0 45px;
}

.nav .navOpenBtn,
.nav .navCloseBtn {
    display: none;
}

/* responsive */
@media screen and (max-width: 1160px) {
    .nav {
        padding: 15px 100px;
    }
    .nav .search-box {
        right: 150px;
    }
}
@media screen and (max-width: 950px) {
    .nav {
        padding: 15px 50px;
    }
    .nav .search-box {
        right: 100px;
        max-width: 400px;
    }
}
@media screen and (max-width: 768px) {
    .nav .navOpenBtn,
    .nav .navCloseBtn {
        display: block;
    }
    .nav {
        padding: 15px 20px;
    }
    .nav .nav-links {
        position: fixed;
        top: 0;
        left: -100%;
        height: 100%;
        max-width: 280px;
        width: 100%;
        padding-top: 100px;
        row-gap: 30px;
        flex-direction: column;
        background-color: #11101d;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        transition: all 0.4s ease;
        z-index: 100;
    }
    .nav.openNav .nav-links {
        left: 0;
    }
    .nav .navOpenBtn {
        color: #ececec;
        font-size: 20px;
        cursor: pointer;
    }
    .nav .navCloseBtn {
        position: absolute;
        top: 20px;
        right: 20px;
        color: #ececec;
        font-size: 20px;
        cursor: pointer;
    }
    .nav .search-box {
        top: calc(100% + 10px);
        max-width: calc(100% - 20px);
        right: 50%;
        transform: translateX(50%);
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    }
}
</style>