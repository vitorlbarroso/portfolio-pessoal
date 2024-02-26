<script>
import Button from "@/components/Button.vue";
import TabsInfos from "@/components/TabsInfos.vue";
import ProjectCard from "@/components/ProjectCard.vue";

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
            },
            projects: [
                {
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1211762849496694834/p_fp.png?ex=65ef6118&is=65dcec18&hm=c4f77e73277769f019c563ef11ec57a74e2f06e836ec567e57dedc5a1050abc9&",
                    title: "Flame Pay",
                    positionAtProject: "Líder de Equipe",
                    description: "Nesse projeto, fui responsável pela contratação de novos desenvolvedores, planejamento de tarefas através de metodologias ágeis e o líder da equipe de desenvolvimento.",
                    projectLink: "https://flamepay.com.br",
                },
                {
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1211762849802625104/p_vp.png?ex=65ef6118&is=65dcec18&hm=bf8cc1e9798e7b8312b06ebe5b840108fadb9b1805afb29a5a12f9f92e907b54&",
                    title: "Vídeo Player",
                    positionAtProject: "Desenvolvedor e Arquiteto",
                    description: "Desenvolvi e arquitetei toda a estrutura do vídeo player. Utilizei Javascript para a criação do Player e Buckets S3, Lambda Func. e o serviço AWS MediaConvert para armazenar e converter os vídeos.",
                    projectLink: null,
                },
                {
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1211762850263994489/p_jm.png?ex=65ef6118&is=65dcec18&hm=b1a4dfcdc93badde1566f93d4d1f5df725112553353b18def1ab246ee9b49c71&",
                    title: "Jump Mario",
                    positionAtProject: "Desenvolvedor",
                    description: "Desenvolvi um game utilizando Javascript. Esse game é um réplica do famoso “Joguinho do Dinossauro”, porém, adaptado ao tema do Super Mário.",
                    projectLink: "https://mario-jump-vitorlbarroso.netlify.app/",
                },
                {
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1211762850666782730/p_hb.png?ex=65ef6119&is=65dcec19&hm=b0e2d63a5b0d133b4fb0f94a4b38de9ba295f2a1de10028c246ce2b45f464d60&",
                    title: "Hit Biz",
                    positionAtProject: "UI/UX Designer",
                    description: "Apliquei técnicas de Design e Experiência do usuário para criar uma melhor experiência para os produtores da plataforma.",
                    projectLink: null,
                },
                {
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1211762850930884679/p_ps.png?ex=65ef6119&is=65dcec19&hm=4e5a639d60364d0c4b086fadb9a3395af93d1b21391e3da6184cc7eea14604af&",
                    title: "Pro Seller",
                    positionAtProject: "Desenvolvedor e Arquiteto",
                    description: "Desenvolvi e arquitetei um sistema voltado para a criação de Landing Pages através de um Page Builder (Estilo WordPress). Nesse projeto, utilizei o Vue.JS, .NET Core 6 e Serviços AWS.",
                    projectLink: null,
                },
                {
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1211768380218937354/p_pp.png?ex=65ef663f&is=65dcf13f&hm=cb16a9547df02e59d15269d7f5af62131d84f677836e8d5c33f13b26361ba83e&",
                    title: "PicPay + PHP",
                    positionAtProject: "Desenvolvedor",
                    description: "Desenvolvi uma biblioteca de adaptação da API do PicPay com o PHP, a fim de facilitar a integração da aplicação para pessoas que queiram vender através da internet.",
                    projectLink: "https://github.com/vitorlbarroso/api-php-picpay",
                },
                {
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1211762849169412096/p_el.png?ex=65ef6118&is=65dcec18&hm=fce1a64f4998006e1e5876d9a0727e1753f117bf1ec8baae0a13b0f809386037&",
                    title: "Essa Loja",
                    positionAtProject: "Desenvolvedor FullStack",
                    description: "Loja desenvolvida utilizando Vue.JS e Laravel. Integrei a essa plataforma, sistema de vendas completo, sistema de envio e rastreio de pacotes via Correios e Melhor Envio",
                    projectLink: null,
                },
            ],
        }
    },
    components: { Button, TabsInfos, ProjectCard },
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

        <section id="projects" class="container">
            <h1>Projetos</h1>
            
            <section id="projects-list">
                <ProjectCard v-for="(project, index) in projects" :data="project" />
            </section>
        </section>
    </div>
</template>

<style src="@/assets/css/home-style.css" scoped></style>