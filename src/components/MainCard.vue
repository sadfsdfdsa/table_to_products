<template>
    <div id="main">
        <b-card :class="style">
            <b-card-body>
                <p>{{body_text}}</p>
            </b-card-body>
        </b-card>
    </div>
</template>

<script>
    export default {
        name: "MainCard",
        props: ['body_text', 'isPrimary'],
        computed: {
            style: function () {
                return this.isPrimary ? 'bg-primary text-white' : 'bg-warning'
            }
        }
    }
</script>

<style scoped>

</style>