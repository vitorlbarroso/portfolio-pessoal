<script>
export default {
    props: {
        data: {
            type: {
                Object,
                required: true,
            }
        }
    },
    methods: {
        closeModal() {
            this.$emit('closeModal', true);
        }
    }
}
</script>

<template>
    <section class="bg-modal">
        <section @click="closeModal" class="click-bg-model"></section>
        <section class="modal">
            <div @click="closeModal" class="close-modal">x</div>

            <h1 class="modal-title">{{ data.title }}</h1>

            <figure>
                <img src="@/assets/img/cat.svg" alt="Vitor Barroso - Modal de Erro">
            </figure>

            <p class="modal-description">{{ data.description }}</p>
        </section>
    </section>
</template>

<style scoped>
    body {
        overflow: hidden !important;
    }

    .bg-modal {
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.891);
        position: fixed;
        bottom: 0px;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-left: -50px;
        z-index: 2;
    }

    .click-bg-model {
        width: 100%;
        height: 100%;
        cursor: pointer;
    }

    .modal {
        width: 500px;
        max-width: 100%;
        padding: 60px 40px;
        height: auto;
        background-color: var(--primary-bg);
        border: 1px solid var(--tertiary-border);
        position: absolute;
        z-index: 4;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        border-radius: 10px;
        text-align: center;
    }

    .close-modal {
        color: var(--tertiary-text);
        position: absolute;
        top: 10px;
        right: 20px;
        cursor: pointer;
    }

    .modal h1 {
        font-size: 24px;
        font-weight: 650;
        background: var(--primary-text-gradient);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        padding-bottom: 40px;
    }

    .modal figure img {
        width: 110px;
        margin-left: 10px;
    }

    .modal p {
        font-size: 16px;
        font-weight: 500;
        padding-top: 40px;
        color: white;
    }

    @media screen and (max-width: 850px) {
    #work-experiences {
        padding-right: 50px;
    }
}

@media screen and (max-width: 640px) {
    .bg-modal,
    .click-bg-model {
        margin-left: 0px !important;
        padding: 0px 20px 0px 0px;
    }

    .modal {
        width: 90%;
    }
}
</style>