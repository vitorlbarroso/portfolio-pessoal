<script>
export default {
    props: {
        data: {
            type: Object,
            required: true
        }
    },
    data() {
        return {
            openErrorCard: false,
        }
    }
}
</script>

<template>
    <section class="bg-project-card">
        <figure>
            <img :src="data.imageLink" alt="Projeto - Vitor Barroso">
        </figure>

        <section class="description-project-card">
            <h1>{{ data.title }}</h1>
            <h2>{{ data.positionAtProject }}</h2>

            <p>{{ data.description }}</p>
        </section>

        <a v-if="data.projectLink != null" :href="data.projectLink" target="_blank" class="button-project-card">
            Visitar projeto
        </a>
        <a v-else @click="openErrorCard = true;" target="_blank" class="button-project-card">
            Visitar projeto
        </a>
    </section>
</template>

<style scoped>
    .bg-project-card {
        width: 260px;
        max-width: 100%;
        height: auto;
        min-height: 370px;
        margin-right: 10px;
        margin-bottom: 10px;
        background: var(--primary-border-gradient);
        border-radius: 8px;
        position: relative;
        padding-bottom: 50px;
    }

    .bg-project-card figure img {
        width: 260px;
        padding: 10px;
    }

    .bg-project-card .description-project-card {
        padding: 0px 10px;
    }

    .bg-project-card .description-project-card h1 {
        font-size: 18px;
        font-weight: 650;
        background: var(--primary-text-gradient);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    .bg-project-card .description-project-card h2 {
        font-size: 15px;
        font-weight: 400;
        color: var(--color-white);
        margin-bottom: 5px;
    }

    .bg-project-card .description-project-card p {
        font-size: 14px;
        color: var(--tertiary-text);
    }

    .button-project-card {
        position: absolute;
        bottom: 0px;
        width: 100%;
        height: auto;
        background: var(--primary-text-gradient);
        text-align: center;
        padding: 8px 0px;
        border-radius: 0px 0px 8px 8px;
        cursor: pointer;
        font-weight: 600;
        color: var(--primary-color);
    }

    .button-project-card:hover {
        color: var(--color-white);
    }

    @media screen and (max-width: 650px) {
        .bg-project-card {
            width: 380px;
            padding-bottom: 100px;
        }

        .bg-project-card figure img {
            width: 100%;
        }

        .bg-project-card .description-project-card {
            padding: 0px 16px;
        }

        .bg-project-card .description-project-card h1 {
            font-size: 26px;
        }

        .bg-project-card .description-project-card h2 {
            font-size: 20px;
        }

        .bg-project-card .description-project-card p {
            font-size: 20px;
        }

        .button-project-card {
            padding: 14px 0px;
            font-size: 18px;
        }
    }
</style>