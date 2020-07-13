<template>
    <div id="main">
        <b-container>
            <b-row class="mt-2" align-h="center">
                <b-col sm="4" :order="order_component_1">
                    <MainCard :body_text="text_1" :is-primary="true"></MainCard>
                </b-col>
                <b-col sm="4">
                    <MainCard :body_text="text_2"></MainCard>
                </b-col>
            </b-row>
            <b-row class="mt-3" align-h="center">
                <b-col sm="1">
                    <b-button @click="swap" variant="success">Swap!</b-button>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import MainCard from "@/components/MainCard";

    export default {
        name: "IndexPage",
        components: {MainCard},
        data: () => ({
            text_1: 'First component',
            text_2: 'Second component',
            order_component_1: 0
        }),
        methods: {
            swap() {
                this.order_component_1 = this.order_component_1 === 1 ? 0 : 1;
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>