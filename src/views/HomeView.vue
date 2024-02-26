<script>
import Button from "@/components/Button.vue";

export default {
    components: { Button },
}
</script>

<template>
    <div>
        <header>
            <router-link class="link" to="">Contato</router-link>
            <router-link class="link" to="">Blog</router-link>
        </header>

        <section id="personal-presentation" class="container">
            <article id="infos-personal-presentation">
                <h1>Vitor Barroso</h1>
                <h2>Desenvolvedor Full Stack</h2>

                <p>Com experiência em desenvolvimento Front-end, Back-end, UI/UX e DevOps, estou a mais de 4 anos transformando e ajudando empresas a alavancarem seus sistemas através da internet.</p>

                <Button text="Baixar CV" type="gradient"></Button>
                <Button text="Entrar em contato" type="gray"></Button>
            </article>

            <figure id="infos-personal-figure">
                <img src="@/assets/img/vitor_barroso_dev_icon.svg" alt="Vitor Barroso">
            </figure>
        </section>
    </div>
</template>

<style scoped>
    header {
        width: 100%;
        height: 60px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    header .link {
        margin: 0px 10px;
        font-size: 16px;
        font-weight: 500;
        color: var(--color-white);
    }

    header .link:hover {
        background: var(--primary-text-gradient);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    #personal-presentation {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        height: auto;
    }

    #infos-personal-presentation h1 {
        font-size: 50px;
        font-weight: bold;
        background: var(--primary-text-gradient);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    #infos-personal-presentation h2 {
        font-size: 32px;
        color: white;
        font-weight: 400;
        margin: 15px 0px;
    }

    #infos-personal-presentation p {
        color: var(--color-gray);
        font-size: 18px;
        max-width: 700px;
        margin-bottom: 30px;
    }

    @media screen and (max-width:1010px) {
        #personal-presentation {
            margin-top: 20px;
        }

        #infos-personal-presentation {
            width: 100%;
            justify-content: center;
            text-align: center;
        }

        #infos-personal-presentation p {
            margin: 0px auto 30px auto;
        }

        #infos-personal-figure {
            display: none;
        }
    }

    @media screen and (max-width:510px) {
        #infos-personal-presentation h1 {
            font-size: 42px;
        }

        #infos-personal-presentation h2 {
            font-size: 26px;
        }
    }
</style>