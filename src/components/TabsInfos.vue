<script>
import Skills from '@/components/Skills.vue';

export default {
    props: {
        data: {
            type: Object,
            required: true,
        }
    },
    data() {
        return {
            isActive: "Pepper",
            isActiveData: {},
        }
    },
    created() {
        this.isActiveData = this.data.Pepper;
    },
    methods: {
        calculateDate(initDate, finalDate) {
            const initDateParts = initDate.split('/');
            const finalDateParts = finalDate.split('/');
            const initDateObj = new Date(initDateParts[2], initDateParts[1] - 1, initDateParts[0]);
            const finalDateObj = new Date(finalDateParts[2], finalDateParts[1] - 1, finalDateParts[0]);

            const diffMilissegundos = finalDateObj - initDateObj;

            const diffAnos = Math.floor(diffMilissegundos / (1000 * 60 * 60 * 24 * 365));
            const diffMeses = Math.floor((diffMilissegundos % (1000 * 60 * 60 * 24 * 365)) / (1000 * 60 * 60 * 24 * 30));

            let resultDate = '';
            if (diffAnos > 0) {
                resultDate += `${diffAnos} ano${diffAnos > 1 ? 's' : ''}`;
            }
            if (diffMeses > 0) {
                if (diffAnos > 0) {
                    resultDate += ` e ${diffMeses} mes${diffMeses > 1 ? 'es' : ''}`;
                } else {
                    resultDate += `${diffMeses} mes${diffMeses > 1 ? 'es' : ''}`;
                }
            }

            const initMonth = initDateObj.toLocaleString('default', { month: 'short' });
            const initYear = initDateObj.getFullYear();
            const finalMonth = finalDateObj.toLocaleString('default', { month: 'short' });
            const finalYear = finalDateObj.getFullYear();

            const finalString = `${initMonth} ${initYear} - ${finalMonth} ${finalYear} (${resultDate})`;
            return finalString;
        },
    },
    components: { Skills }
}
</script>

<template>
    <section class="bg-tabs-infos">
        <nav class="bg-tab">
            <div 
                v-for="(item, index) in data" 
                :class="[isActive == index ? 'is-active' : '', 'tab']"
                @click="isActiveData = item; isActive = index">
                {{ index }}
            </div>
        </nav>

        <article class="content-tab">
            <h2>{{ isActiveData.positionAtWork }}</h2>
            <h4>{{ calculateDate(isActiveData.startedIn, isActiveData.finishedIn) }}</h4>
            <h3>{{ isActive }}</h3>

            <p>{{ isActiveData.description }}</p>

            <Skills :data="isActiveData.skills" />
        </article>
    </section>
</template>

<style scoped>
    .bg-tabs-infos {
        width: 100%;
        display: flex;
        align-items: flex-start;
        justify-content: flex-start;
    }

    .tab {
        width: 100%;
        max-width: 220px;
        color: white;
        cursor: pointer;
        padding: 14px 24px;
        border-left: 3px solid transparent;
        background-color: var(--primary-bg);
        font-weight: 500;
    }

    .tab:hover {
        background-color: rgb(30, 30, 30);
    }

    .is-active {
        border-left: 3px solid var(--color-green);
    }
    
    .content-tab {
        max-width: 80%;
        padding: 0px 20px;
    }

    .content-tab p,
    .content-tab h2,
    .content-tab h3,
    .content-tab h4 {
        margin-bottom: 8px;
    }

    .content-tab h2 {
        font-size: 20px;
        background: var(--primary-text-gradient);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        font-weight: 650;
    }

    .content-tab h4 {
        font-size: 16px;
        color: var(--tertiary-text);
        font-weight: 400;
    }

    .content-tab h3 {
        font-size: 18px;
        background: var(--primary-text-gradient);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        font-weight: 650;
    }

    .content-tab p {
        font-size: 17px;
        color: var(--tertiary-text);
        font-weight: 400;
    }

    @media screen and (max-width:850px) {
        .bg-tabs-infos {
            flex-direction: column;
        }

        .bg-tab {
            width: 100%;
        }

        .tab {
            max-width: 100%;
        }

        .content-tab {
            max-width: 100%;
            margin: 30px 0px;
            min-height: 260px;
            padding: 0px;
        }
    }
</style>