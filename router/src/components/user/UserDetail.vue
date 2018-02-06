<template>
    <div>
        <h3>Some User Details {{ id }}</h3>
        <router-link
                tag="button"
                :to="link"
                class="btn btn-primary">Edit
        </router-link>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                id: this.$route.params.id,
                link: {
                    name: 'userEdit',
                    id: this.id,
                    hash: '#data'
                }
            }
        },
        beforeRouteEnter(to, from, next){

            next();
        }
    }
</script>