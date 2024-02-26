<script>
export default {
    props: {
        text: {
            type: String,
            required: true,
        },
        type: {
            type: String,
            required: true,
        }
    }
}
</script>

<template>
    <div>
        <button :class="[type == 'gradient' ? 'gradient' : 'gray', 'button']">
            <p>{{ text }}</p>
        </button>
    </div>
</template>

<style scoped>
.button {
    padding: 14px 36px;
    border-radius: 10px;
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
    color: var(--color-dark);
    margin-bottom: 10px;
}

.gradient {
    background: var(--primary-text-gradient);
    border: none;
}

.gradient:hover {
    background: var(--primary-border-gradient);
    border-radius: 8px;
}

.gradient:hover p {
    background: var(--primary-text-gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.gray {
    background: var(--secondary-text-gradient);
    border: none;
}

.gray:hover {
    background: var(--secondary-border-gradient);
    border-radius: 8px;
}

.gray:hover p {
    background: var(--secondary-text-gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
</style>

