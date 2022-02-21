<script>
    export default {
        data() {
            return {
                links: [
                    {
                        name: 'HOME',
                        route: 'Home'
                    },
                    {
                        name: 'DESTINATION',
                        route: 'Home'
                    },
                    {
                        name: 'CREW',
                        route: 'Home'
                    },
                    {
                        name: 'TECHNOLOGY',
                        route: 'Home'
                    },
                ]
            }
        }   
    }
</script>

<template>
    
    <header>

        <router-link :to="{name: 'Home'}">
            <img src="@/assets/img/shared/logo.svg" alt="Logo" class="logo">
        </router-link>

        <hr>

        <nav>

            <ul>
                <li v-for="link, index in links" :key="index" > 
                    <router-link :to="link.route" > <span class="marker"> {{ "0" + (index+1) }} </span> {{ link.name }} </router-link>
                </li>
            </ul>

        </nav>

    </header>

</template>

<style lang="scss" scoped>

    @import "../assets/styles/variables";

    header {
        padding-left: 50px;
        display: flex;
        align-items: center;

        hr {
            display: none;
            background-color: #FFFFFF;
            opacity: 0.25;

            @media (min-width: 768px) {
                display: block;
                width: 40%;
                margin-right: -5%;
            }
        }

        nav {
            position: relative;
            width: 55%;
            height: 95px;
            display: flex;
            align-items: center;
            font: $nav-text;
            margin-left: auto;
            background: rgba(255, 255, 255, 0.04);
            -webkit-backdrop-filter: blur(81.5485px);
            backdrop-filter: blur(81.5485px);

            ul {
                list-style-type: none;
                margin: 0;
                padding: 0;
                margin-left: 2.5rem;

                li {
                    display: inline-block;
                    margin-left: 2.5rem;

                    a {
                        text-decoration: none;
                        color: $white;
                        letter-spacing: 2.7px;
                        .marker {
                            font-weight: bold;
                            margin-right: .5rem;
                        }
                    }
                }
            }
        }
    }

</style>