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

            <button v-for="(contact, index) in data.contacts" class="button-contact">
                <a :href="contact.link" target="_blank"> {{ contact.name }} </a>
            </button>
        </section>
    </section>
</template>

<style scoped>
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

    .button-contact {
        width: 80%;
        padding: 16px 0px;
        background: var(--primary-text-gradient);
        border: 1px solid transparent;
        border-radius: 5px;
        font-size: 18px;
        font-weight: 700;
        margin-bottom: 10px;
        cursor: pointer;
    }

    .button-contact a {
        color: var(--color-dark);
    }

    .button-contact:hover {
        background: var(--primary-border-gradient);
        border-radius: 8px;
    }

    .button-contact:hover a {
        background: var(--primary-text-gradient);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
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