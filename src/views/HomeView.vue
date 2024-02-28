<script>
import Button from "@/components/Button.vue";
import TabsInfos from "@/components/TabsInfos.vue";
import ProjectCard from "@/components/ProjectCard.vue";
import HoverExperiences from "@/components/HoverExperiences.vue";
import Footer from "@/components/Footer.vue";
import ModalError from "@/components/ModalError.vue";
import ModalContact from "@/components/ModalContact.vue";

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
            languagesExperiences: [
                {
                    languageName: "HTML5",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212079026940682260/html5.png?ex=65f0878f&is=65de128f&hm=2967471e1023ce0239d35e2c29d19f43fc90cba840654580f1032b65bf1c9da5&",
                    description: "HTML é uma linguagem de marcação usada para criar e estruturar páginas da web. Composta por elementos e tags, HTML permite a formatação de texto, incorporação de imagens, links e outros recursos multimídia. É a espinha dorsal da web, fornecendo a base para a criação e exibição de conteúdo na internet, sendo interpretada pelos navegadores para apresentar informações de maneira visualmente coerente aos usuários.",
                },
                {
                    languageName: "CSS3",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212081034791886850/css.png?ex=65f0896e&is=65de146e&hm=66110f754b0c8034bd7ddfd79e667151fb137e8edcbcfdc25a5c73e996f42b7b&",
                    description: "CSS é uma linguagem de estilo utilizada para controlar a apresentação visual de páginas da web, separando o conteúdo estrutural (HTML) da sua aparência. Com recursos avançados como seletores, propriedades e valores, o CSS3 permite definir cores, fontes, espaçamento, layout e outros aspectos visuais de forma flexível e eficiente. Ele possibilita a criação de designs atrativos, responsivos e acessíveis, melhorando a experiência do usuário na navegação pela web.",
                },
                {
                    languageName: "Javascript",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212081036289122374/js.png?ex=65f0896e&is=65de146e&hm=7a41e18d48d4607a41de8d76bd5cb6dddc5d274ba32fd1f46f558fd5b96b82ab&",
                    description: "JavaScript é uma linguagem de programação amplamente utilizada para criar interatividade em páginas da web. Como uma linguagem de script do lado do cliente, ela permite manipular o conteúdo HTML e CSS, responder a eventos do usuário e interagir com serviços web, tornando as páginas mais dinâmicas e funcionais.",
                },
                {
                    languageName: "Vue.js",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212081044317012008/vue.png?ex=65f08970&is=65de1470&hm=6454518cd2c86f6edd85d0c7a3322003ef253a1314361397045f9b2282181f9b&",
                    description: "Vue.js é um framework progressivo de JavaScript utilizado para construir interfaces de usuário interativas e reativas. Com uma sintaxe simples e flexível, Vue.js simplifica o desenvolvimento front-end, facilitando a criação de componentes reutilizáveis, gerenciamento de estado e integração com outras bibliotecas e ferramentas.",
                },
                {
                    languageName: "Bootstrap",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212081034489757786/bs.png?ex=65f0896d&is=65de146d&hm=c25f65f95148c67b30533b46ad39e7ef39ddd1711e2a81c95a1c9432aa7518fa&",
                    description: "Bootstrap é um framework front-end de código aberto utilizado para desenvolver rapidamente interfaces web responsivas e estilizadas. Com uma coleção de componentes e estilos pré-definidos, Bootstrap simplifica o processo de design, garantindo consistência visual e compatibilidade com diversos dispositivos e navegadores.",
                },
                {
                    languageName: "TailwindCSS",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212081044946161674/tailwindcss.png?ex=65f08970&is=65de1470&hm=af50917a69154ec7a69ccd3b1a72180d5e5edbba7870c782fe72824e1cdb7916&",
                    description: "Tailwind CSS é uma biblioteca de classes CSS utilitárias que permite criar designs personalizados de forma rápida e eficiente. Em vez de fornecer componentes pré-estilizados, o Tailwind CSS fornece uma abordagem mais granular, permitindo estilizar elementos diretamente no HTML com classes específicas, oferecendo maior flexibilidade e controle sobre o design.",
                },
                {
                    languageName: "Laravel",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212081033990897684/laravel.png?ex=65f0896d&is=65de146d&hm=f0bc452a6482c4697a23bed424441621a221e2a64bad91eb78141e31c33c2bd9&",
                    description: "Laravel é um framework de desenvolvimento web em PHP que oferece uma estrutura robusta e elegante para construir aplicativos web modernos e escaláveis. Com recursos como Eloquent ORM, Blade templating engine e Laravel Mix, Laravel simplifica tarefas comuns de desenvolvimento, promovendo uma experiência de programação agradável e produtiva.",
                },
                {
                    languageName: ".NET Core",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212081035123101746/dotnet.png?ex=65f0896e&is=65de146e&hm=d85af29292faf1be5b44a563db164bd4a42bda82793cf537ab7a9c4ac009b313&",
                    description: ".NET Core é uma plataforma de desenvolvimento open-source da Microsoft utilizada para criar aplicativos modernos e escaláveis para web, desktop e dispositivos móveis. Com suporte multiplataforma e uma vasta biblioteca de APIs, o .NET Core oferece desempenho e flexibilidade, permitindo aos desenvolvedores construir e implantar aplicativos em diferentes ambientes de hospedagem.",
                },
                {
                    languageName: "AWS",
                    imageLink: "https://cdn.discordapp.com/attachments/890042596112601120/1212081034250948618/aws.png?ex=65f0896d&is=65de146d&hm=8c54888e84029329697dd6a394336013fdf51b2f06286b2896cfc4cb48e91301&",
                    description: "AWS é uma plataforma de serviços de computação em nuvem fornecida pela Amazon. Oferecendo uma ampla gama de serviços, como computação, armazenamento, banco de dados, machine learning e muito mais, a AWS permite as empresas escalar e gerenciar recursos de forma flexível, segura e econômica, impulsionando a inovação e o crescimento digital.",
                },
            ],
            modalError: {
                isOpened: false,
                title: "",
                description: "",
            },
            modalContact: {
                isOpened: false,
                title: "CONTATO",
                contacts: [
                    {
                        name: "WhatsApp",
                        link: "https://api.whatsapp.com/send/?phone=%2B5527999971368&text=Ol%C3%A1,%20Vitor.%20Peguei%20o%20seu%20contato%20na%20sua%20p%C3%A1gina%20pessoal.%20Est%C3%A1%20podendo%20falar?&type=phone_number&app_absent=0",
                    },
                    {
                        name: "Instagram",
                        link: "https://www.instagram.com/vitorlbarroso/",
                    },
                    {
                        name: "LinkedIn",
                        link: "https://www.linkedin.com/in/vitorlbarroso2004/",
                    },
                    {
                        name: "E-mail",
                        link: "mailto:vitorlauvresbarroso@gmail.com",
                    },
                ]
            },
        }
    },
    methods: {
        openModalContact() {
            this.modalContact.isOpened = true;
        },
        closeModalContact() {
            this.modalContact.isOpened = false;
        },
        openModalError(title, description) {
            this.modalError.title = title;
            this.modalError.description = description;
            this.modalError.isOpened = true;
        },
        closeModalError() {
            this.modalError.isOpened = false;
            this.modalError.title = "";
            this.modalError.description = "";
        },
        downloadCV() {
            const link = document.createElement('a');
            // Define o atributo 'href' do elemento 'a' com o caminho para o arquivo
            link.href = 'https://cdn.discordapp.com/attachments/890042596112601120/1212372188297171014/cv_vitorbarroso.pdf?ex=65f19896&is=65df2396&hm=b99f3ed487d3145ec638737bece1f11df069d7044f88cf8116fc30d562a24474&'; // Substitua com o caminho real do arquivo
            // Define o atributo 'download' para que o navegador faça o download ao invés de navegar para o link
            link.download = 'cv_vitorbarroso.pdf'; // Substitua com a extensão real do arquivo
            // Adiciona o elemento 'a' ao documento
            document.body.appendChild(link);
            // Simula um clique no link para iniciar o download
            link.click();
            // Remove o elemento 'a' do documento
            document.body.removeChild(link);
        },
    },
    components: { Button, TabsInfos, ProjectCard, HoverExperiences, Footer, ModalError, ModalContact },
}
</script>

<template>
    <div>
        <ModalError v-if="modalError.isOpened" @closeModal="closeModalError" :data="modalError" />
        <ModalContact v-if="modalContact.isOpened" @closeModal="closeModalContact" :data="modalContact" />

        <header>
            <router-link class="link" to="" @click="openModalContact">Contato</router-link>
            <router-link class="link" to="" @click="openModalError('EM BREVE!', 'Em breve disponibilizaremos nosso DevBlog com diversos conteúdos exclusivos sobre tecnologia. Fique ligado!')">Blog</router-link>
        </header>

        <section id="personal-presentation" class="container">
            <article id="infos-personal-presentation">
                <h1>Vitor Barroso</h1>
                <h2>Desenvolvedor Full Stack</h2>

                <p>Com experiência em desenvolvimento Front-end, Back-end, UI/UX e DevOps, estou a mais de 4 anos transformando e ajudando empresas a alavancarem seus sistemas através da internet.</p>

                <Button text="Baixar CV" type="gradient" @clickButton="downloadCV"></Button>
                <Button text="Entrar em contato" type="gray" @clickButton="openModalContact"></Button>
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
                <ProjectCard v-for="(project, index) in projects" :data="project" @openModalError="openModalError('INDISPONÍVEL!', 'Infelizmente esse conteúdo não está mais disponível. Entre em contato com o Vitor para mais explicações!')" />
            </section>
        </section>

        <section id="languages-experiences">
            <section class="container">
                <h1>Conhecimentos</h1>
                
                <HoverExperiences :data="languagesExperiences" />
            </section>
        </section>

        <Footer />
    </div>
</template>

<style src="@/assets/css/home-style.css" scoped></style>