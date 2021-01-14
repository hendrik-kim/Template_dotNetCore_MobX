<template>
    <div>x</div>
</template>

<script>
export default {
    data() {
        return {
            bookable: null
        };
    },
    created() {
        console.log(this.$route.params.id);
        axios
            .get(`/api/bookables/${this.$route.params.id}`)
            .then(res => (this.bookable = res.data));
    }
};
</script>

<style lang="scss" scoped></style>
