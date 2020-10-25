<template>
    <div>
        {{ name }}

        <button @click="onChange">
            바꾸기
        </button>
    </div>
</template>

<script>
export default {
    props: {
        name: { type: String, default: '' }
    },
    methods: {
        onChange() {
            this.$emit('change', '박지호')
        }
    }
}
</script>