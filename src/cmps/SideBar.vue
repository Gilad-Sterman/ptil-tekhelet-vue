<template>
    <section className="side-bar">
        <ul>
            <li>
                <a href="#card1" :class="{ active: currCard('card1') }">התרבות המינואית</a>
            </li>
            <li>
                <a href="#card2" :class="{ active: currCard('card2') }">אברהם</a>
            </li>
            <li>
                <a href="#card3" :class="{ active: currCard('card3') }">טבליות אל-עמרנה</a>
            </li>
            <li>
                <a href="#card4" :class="{ active: currCard('card4') }">יהודה ותמר</a>
            </li>
            <li>
                <a href="#card5" :class="{ active: currCard('card5') }">יעקב ובניו</a>
            </li>
            <li>
                <a href="#card6" :class="{ active: currCard('card6') }">יציאת מצרים</a>
            </li>
            <li>
                <a href="#card7" :class="{ active: currCard('card7') }">לפיס לזולי</a>
            </li>
            <li>
                <a href="#card8" :class="{ active: currCard('card8') }">המשכן</a>
            </li>
            <li>
                <a href="#card9" :class="{ active: currCard('card9') }">הכהן הגדול</a>
            </li>
            <li>
                <a href="#card10" :class="{ active: currCard('card10') }">בית המקדש</a>
            </li>
            <li>
                <a href="#card11" :class="{ active: currCard('card11') }">הגלילים האשוריים</a>
            </li>
            <li>
                <a href="#card12" :class="{ active: currCard('card12') }">חורבן נבוכדנצר</a>
            </li>
            <li>
                <a href="#card13" :class="{ active: currCard('card13') }">מרדכבי היהודי</a>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    data() {
        return {
            activeLink: null
        }
    },
    created() {
        window.addEventListener('scroll', this.handleScroll)
    },
    methods: {
        handleScroll() {
            const card2 = document.getElementById('card2')
            const card3 = document.getElementById('card3')
            const card4 = document.getElementById('card4')
            const card5 = document.getElementById('card5')
            const card6 = document.getElementById('card6')
            const card7 = document.getElementById('card7')
            const card8 = document.getElementById('card8')
            const card9 = document.getElementById('card9')
            const card10 = document.getElementById('card10')
            const card11 = document.getElementById('card11')
            const card12 = document.getElementById('card12')
            const card13 = document.getElementById('card13')

            if (window.scrollY < card2.offsetTop - 100) {
                this.activeLink = 'card1'
            } else if (window.scrollY < card3.offsetTop - 100) {
                this.activeLink = 'card2'
            } else if (window.scrollY < card4.offsetTop - 100) {
                this.activeLink = 'card3'
            } else if (window.scrollY < card5.offsetTop - 100) {
                this.activeLink = 'card4'
            } else if (window.scrollY < card6.offsetTop - 100) {
                this.activeLink = 'card5'
            } else if (window.scrollY < card7.offsetTop - 100) {
                this.activeLink = 'card6'
            } else if (window.scrollY < card8.offsetTop - 100) {
                this.activeLink = 'card7'
            } else if (window.scrollY < card9.offsetTop - 100) {
                this.activeLink = 'card8'
            } else if (window.scrollY < card10.offsetTop - 100) {
                this.activeLink = 'card9'
            } else if (window.scrollY < card11.offsetTop - 100) {
                this.activeLink = 'card10'
            } else if (window.scrollY < card12.offsetTop - 100) {
                this.activeLink = 'card11'
            } else if (window.scrollY < card13.offsetTop - 100) {
                this.activeLink = 'card12'
            }
            else {
                this.activeLink = 'card13'
            }
        },
        currCard(card) {
            return this.activeLink === card
        }
    }
}
</script>

<style lang="scss">
.side-bar {
    ul {
        padding-inline-start: 0;
        margin: 0;

        li {
            list-style: none;
            margin-inline-start: 0;
            margin-bottom: .5rem;

            a {
                font-size: 20px;
                color: white;

                &.active {
                    font-size: 36px;
                    line-height: 36px;
                }

                &:hover {
                    color: #e6f4e9;
                }
            }
        }
    }
}
</style>