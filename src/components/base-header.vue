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

        <nav>

            <ul>
                <li v-for="link, index in links" :key="index" > 
                    <router-link :to="link.route" > {{ link.name }} </router-link>
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
                    }
                }
            }
        }
    }

</style>