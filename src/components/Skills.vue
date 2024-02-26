<script>
export default {
    props: {
        data: {
            type: Object,
            required: true
        }
    }
}
</script>

<template>
    <section class="skills-bg">
        <article v-for="(skill, index) in data" class="skill">
            {{ skill }}
            <div v-if="index < (data.length - 1)" class="division-skill"></div>
        </article>
    </section>
</template>

<style scoped>
    .skills-bg {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: flex-start;
        flex-wrap: wrap;
    }

    .skill {
        color: var(--color-white);
        font-size: 14px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .division-skill {
        width: 5px;
        height: 5px;
        border-radius: 100%;
        background: var(--primary-text-gradient);
        margin: 0px 6px;
    }
</style>