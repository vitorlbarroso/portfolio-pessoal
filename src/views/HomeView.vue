<script>
import Button from "@/components/Button.vue";
import TabsInfos from "@/components/TabsInfos.vue";

export default {
    data() {
        return {
            workingExperiencesList: {
                "Pepper": {
                    positionAtWork: "Desenvolvedor Full Stack",
                    startedIn: "01/09/2022",
                    finishedIn: "01/02/2024",
                    description: "Durante esse período na Pepper, fui responsável pelo desenvolvimento e manutenção de novas plataformas públicas e internas da empresa. Um dos projetos de maior destaque, onde fui o principal desenvolvedor front-end e back-end, possui hoje, mais de 1 milhão de usuário e uma média de 300 mil usuários ativos/mês.",
                    skills: [
                        "HTML5",
                        "CSS3",
                        "TailwindCSS",
                        "Vue.js",
                        "C#",
                        ".NET Core",
                        "Entity Framework",
                        "LINQ",
                        "PHP",
                        "Laravel",
                        "AWS",
                        "UI/UX",
                        "Figma",
                        "Metodologias Agile",
                        "Jira",
                    ]
                },
                "Cometa Code": {
                    positionAtWork: "Desenvolvedor Full Stack",
                    startedIn: "01/01/2022",
                    finishedIn: "01/10/2023",
                    description: "Fui responsável por liderar projetos para empresas de pequeno e médio porte, além de ter sido o responsável pelo desenvolvimento de sistemas web, mobile e desktop.",
                    skills: [
                        "HTML5",
                        "CSS3",
                        "TailwindCSS",
                        "Bootstrap",
                        "JQuery",
                        "Vue.js",
                        "PHP",
                        "Laravel",
                        "AWS",
                        "MySQL",
                        "UI/UX",
                    ]
                },
                "HZZ Devs": {
                    positionAtWork: "Desenvolvedor Back-end",
                    startedIn: "01/04/2021",
                    finishedIn: "01/12/2021",
                    description: "Trabalhei arquitetando e desenvolvendo projetos para uma plataforma da Rockstar Games (FiveM, onde tive grandes desafios com empresários e investidores do setor, trazendo soluções inovadoras e lucrativas para seus negócios.",
                    skills: [
                        "Lua",
                        "C#",
                        "vRP 1.0",
                        "Cfx.re",
                        "FiveM",
                        "Natives",
                    ]
                },
                "Space Design": {
                    positionAtWork: "Designer Gráfico",
                    startedIn: "01/07/2020",
                    finishedIn: "01/01/2021",
                    description: "Trabalhei na formulação e criação de criativos, logos e flyers para empresas, a fim de proporcionar um Marketing mais inteligente e gerar conversão de clientes e vendas.",
                    skills: [
                        "Canva",
                        "Adobe Photoshop",
                        "Mídias Sociais",
                        "Adobe Illustrator",
                        "Marketing Digital",
                        "Design Gráfico",
                        "Meta ADS",
                    ]
                },
                "Verde Sião Agrop.": {
                    positionAtWork: "Vendedor",
                    startedIn: "01/10/2017",
                    finishedIn: "01/10/2020",
                    description: "Vendedor, assistente geral e designer gráfico, atuei auxiliando no sistema de gestão da empresa, prestando atendimentos, vendas e criando artes para as mídias sociais da empresa.",
                    skills: [
                        "Adobe Photoshop",
                        "Atendimento ao cliente",
                        "Banco de dados relacional",
                        "Sistemas PDV",
                        "Vendas",
                        "Varejo",
                    ]
                },
            }
        }
    },
    components: { Button, TabsInfos },
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

        <section id="about-me" class="container">
            <figure id="infos-about-me-figure">
                <img src="@/assets/img/vitor_barroso_profile.svg" alt="Vitor Barroso">
            </figure>

            <article id="infos-about-me">
                <h3>Quem sou</h3>
                <h2>Vitor Barroso</h2>
                <h4>Desenvolvedor Full Stack Pleno</h4>

                <p>
                    Apaixonado por tecnologias desde criança, comecei a programar com apenas 11 anos, na linguagem Java. Apesar de ser fissurado por tecnologias, ingressei no mercado de trabalho na área de T.I. Em 2020.
                </p>

                <p>
                    Nesse meio tempo, adquiri vasta experiência com desenvolvimento Front-end, Back-end, técnicas de UI e UX, Design e DevOps.
                </p>

                <p>
                    Atualmente, trabalhando com as tecnologias Vue.js, .Net 6 e Laravel. Possuo a versatilidade de trabalhar com qualquer tecnologia que seja necessária para a execução do trabalho.
                </p>
            </article>
        </section>

        <section id="work-experiences">
            <section class="container">
                <h1>Experiências</h1>
                <TabsInfos :data="workingExperiencesList" />
            </section>
        </section>
    </div>
</template>

<style scoped>
    /* Header */
    header {
        width: 100%;
        height: 90px;
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

    /* Apresentação pessoal */
    #personal-presentation {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        height: auto;
        margin-top: -30px;
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

    /* Sobre mim */
    #about-me {
        width: 100%;
        height: auto;
        background-color: var(--secondary-bg);
        border: 1px solid var(--tertiary-border);
        border-radius: 10px;
        margin: 50px auto;
        padding: 20px;
        display: flex;
        align-items: flex-start;
        justify-content: flex-start;
    }

    #infos-about-me-figure img {
        width: 100%;
        max-width: 400px;
    }

    #infos-about-me {
        max-width: 70%;
        padding: 10px 20px;
    }

    #infos-about-me h3 {
        font-size: 18px;
        font-weight: 600;
        background: var(--primary-text-gradient);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    #infos-about-me h2 {
        font-size: 26px;
        margin: 6px 0px;
        color: var(--color-white);
    }

    #infos-about-me h4 {
        font-size: 18px;
        font-weight: 400;
        color: var(--color-white);
    }

    #infos-about-me p {
        color: var(--tertiary-text);
        margin-top: 15px;
        line-height: 20px;
    }

    #work-experiences h1 {
        font-size: 28px;
        color: var(--color-white);
        font-weight: 600;
        margin-bottom: 20px;
    }

    /* Tablet */
    @media screen and (max-width:1010px) {
        /* Apresentação pessoal */
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

        /* Sobre mim */
        #about-me {
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        #infos-about-me-figure {
            width: 100%;
        }

        #infos-about-me {
            max-width: 100%;
            padding: 10px 10px;
        }

        #infos-about-me h3 {
            font-size: 18px;
        }

        #infos-about-me h2 {
            font-size: 28px;
        }
    }

    /* Mobile */
    @media screen and (max-width:510px) {
        /* Apresentação pessoal */
        #infos-personal-presentation h1 {
            font-size: 42px;
        }

        #infos-personal-presentation h2 {
            font-size: 26px;
        }
    }
</style>