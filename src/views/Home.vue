<template>

    <main>

        <div class="container">

            <section class="col-12 col-lg-4">

                <h5 class="text-blue"> SO, YOU WANT TO TRAVEL TO </h5>

                <h1> SPACE </h1>

                <p>Let’s face it; if you want to go to space, you might as well genuinely go to outer space and not hover kind of on the edge of it. Well sit back, and relax because we’ll give you a truly out of this world experience!</p>

            </section>

        </div>

    </main>

</template>

<style lang="scss" scoped>

    main {
        height: 100%;
        background-image: url('../assets/img/home/background-home-desktop.jpg');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        display: flex;
        align-items: flex-end;

        .container {
            margin-bottom: 50px;

            @media (min-width: 768px) {
                margin-bottom: 90px;
            }
            @media (min-width: 1400px) {
                margin-bottom: 130px;
            }
        }
    }

</style>