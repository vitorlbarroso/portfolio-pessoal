<script>
export default {
    props: {
        data: {
            required: true,
            type: Object,
        }
    },
    data() {
        return {
            selectedLanguage: null,
        }
    },
}
</script>

<template>
    <section class="bg-hover-experiences">
        <section class="hover-icons">
            <div 
                v-for="(experience, index) in data" 
                @mouseover="selectedLanguage = experience" 
                @mouseleave="selectedLanguage = null" 
                class="icon"
            >
                <img :src="experience.imageLink" alt="Vitor Barroso - Conhecimentos">
            </div>
        </section>

        <section class="content-experience">
            <h2 v-if="selectedLanguage != null">{{ selectedLanguage.languageName }}</h2>

            <p>{{ selectedLanguage != null ? selectedLanguage.description : "*Passe o mouse pelo card para ler.*" }}</p>
        </section>
    </section>
</template>

<style scoped>
.bg-hover-experiences {
    width: 100%;
    height: auto;
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
}

.hover-icons {
    max-width: 500px;
    width: 100%;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    grid-gap: 10px;
}

.icon {
    background: var(--primary-bg);
    border: 1px solid var(--tertiary-border);
    border-radius: 5px;
    width: 150px;
    height: 150px;
    transition: 0.3s;
    display: flex;
    align-items: center;
    justify-content: center;
}

.icon:hover {
    border: 1px solid var(--color-green);
    cursor: pointer;
    transition: 0.3s;
}

.icon img {
    width: 50%;
}

.content-experience {
    max-width: 50%;
    font-size: 18px;
    color: var(--tertiary-text);
    padding: 0px 20px;
}

.content-experience h2 {
    font-size: 24px;
    font-weight: 650;
    background: var(--primary-text-gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 10px;
}

@media screen and (max-width:910px) {
    .bg-hover-experiences {
        flex-direction: column;
    }

    .content-experience {
        max-width: 90%;
        margin-top: 30px;
        padding: 0px;
    }
}

@media screen and (max-width: 550px) {
    .hover-icons {
        max-width: 100%;
        grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
        grid-gap: 10px;
    }

    .icon {
        width: 100px;
        height: 100px;
        margin-left: 10px;
    }
}
</style>