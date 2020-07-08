<template>
    <v-app>
        <v-main transition="slide-x-transition">
            <router-view></router-view>
        </v-main>
        <div class="sections-menu">
            <span class="menu-point" v-bind:class="{active: activeSection == index}" v-on:click="scrollToSection(index)"
                v-for="(offset, index) in offsets" v-bind:key="index">
            </span>
        </div>
        <v-btn fixed icon bottom color="transparent" style="bottom: 16px !important;">
            <v-icon color="black" large class="arrow-down">mdi-arrow-down</v-icon>
        </v-btn>
        <div class="background-gradient"></div>
    </v-app>
</template>

<style>
    * {
        z-index: 1;
    }

    .background-gradient {
        z-index: 0 !important;
        width: 100vw;
        height: 100vh;
        position: fixed;
        top: 0;
        left: 0;
        background: #14d0e5;
        /* Old browsers */
        background: -moz-linear-gradient(left, #14d0e5 0%, #278df4 50%, #2f52bc 100%);
        /* FF3.6-15 */
        background: -webkit-linear-gradient(left, #14d0e5 0%, #278df4 50%, #2f52bc 100%);
        /* Chrome10-25,Safari5.1-6 */
        background: linear-gradient(to right, #14d0e5 0%, #278df4 50%, #2f52bc 100%);
        /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#14d0e5', endColorstr='#2f52bc', GradientType=1);
    }


    .fill-height {
        height: 100vh !important;
    }

    /*
    ::-webkit-scrollbar {
        display: none;
    }

    #app {
        -ms-overflow-style: none;

        scrollbar-width: none;

    }

    .sections-menu {
        position: fixed;
        right: 1rem;
        top: 50%;
        transform: translateY(-50%);
    }

    .sections-menu .menu-point {
        width: 10px;
        height: 10px;
        background-color: rgb(33,33,33);
        border: none;
        box-shadow: none;
        display: block;
        margin: 1rem 0;
        opacity: .5;
        transition: .8s ease all;
        cursor: pointer;
    }

    .sections-menu .menu-point.active {
        opacity: 1;
        transform: scale(1.5);
    }
    */
</style>

<script>
    export default {
        name: 'App',
        data: () => {
            return {
                //    inMove: false,
                //    activeSection: 0,
                //    offsets: [],
                //    touchStartY: 0
            }
        },
        methods: {
            // calculateSectionOffsets() {
            //     let sections = document.querySelectorAll('.section');
            //     console.log(sections);
            //     let length = sections.length;
            //
            //     for (let i = 0; i < length; i++) {
            //         let sectionOffset = sections[i].offsetTop;
            //         this.offsets.push(sectionOffset);
            //     }
            // },
            // handleMouseWheel: function (e) {
            //
            //     if (e.wheelDelta < 30 && !this.inMove) {
            //         this.moveUp();
            //     } else if (e.wheelDelta > 30 && !this.inMove) {
            //         this.moveDown();
            //     }
            //
            //     e.preventDefault();
            //     return false;
            // },
            // handleMouseWheelDOM: function (e) {
            //
            //     if (e.detail > 0 && !this.inMove) {
            //         this.moveUp();
            //     } else if (e.detail < 0 && !this.inMove) {
            //         this.moveDown();
            //     }
            //
            //     return false;
            // },
            // moveDown() {
            //     this.inMove = true;
            //     this.activeSection--;
            //
            //     if (this.activeSection < 0) this.activeSection = this.offsets.length - 1;
            //
            //     this.scrollToSection(this.activeSection, true);
            // },
            // moveUp() {
            //     this.inMove = true;
            //     this.activeSection++;
            //
            //     if (this.activeSection > this.offsets.length - 1) this.activeSection = 0;
            //
            //     this.scrollToSection(this.activeSection, true);
            // },
            // scrollToSection(id, force = false) {
            //     if (this.inMove && !force) return false;
            //
            //     this.activeSection = id;
            //     this.inMove = true;
            //
            //     document.querySelectorAll('.section')[id].scrollIntoView({
            //         behavior: 'smooth'
            //     });
            //
            //     setTimeout(() => {
            //         this.inMove = false;
            //     }, 400);
            //
            // },
            // touchStart(e) {
            //     e.preventDefault();
            //
            //     this.touchStartY = e.touches[0].clientY;
            // },
            // touchMove(e) {
            //     if (this.inMove) return false;
            //     e.preventDefault();
            //
            //     const currentY = e.touches[0].clientY;
            //
            //     if (this.touchStartY < currentY) {
            //         this.moveDown();
            //     } else {
            //         this.moveUp();
            //     }
            //
            //     this.touchStartY = 0;
            //     return false;
            // }
        },
        mounted() {
            //this.calculateSectionOffsets();
            //
            //window.addEventListener('DOMMouseScroll', this.handleMouseWheelDOM); // Mozilla Firefox
            //window.addEventListener('mousewheel', this.handleMouseWheel, {
            //    passive: false
            //}); // Other browsers
            //
            //window.addEventListener('touchstart', this.touchStart, {
            //    passive: false
            //}); // mobile devices
            //window.addEventListener('touchmove', this.touchMove, {
            //    passive: false
            //}); // mobile devices
        },
        destroyed() {
            //window.removeEventListener('mousewheel', this.handleMouseWheel, {
            //    passive: false
            //}); // Other browsers
            //window.removeEventListener('DOMMouseScroll', this.handleMouseWheelDOM); // Mozilla Firefox
            //
            //window.removeEventListener('touchstart', this.touchStart); // mobile devices
            //window.removeEventListener('touchmove', this.touchMove); // mobile devices
        }
    };
</script>