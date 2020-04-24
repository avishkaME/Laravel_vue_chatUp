<template>
    <div >
        <li class="list-group-item" :class="colorClass"><slot></slot></li>
        <small class="badge float-right" :class="badgeClass">You</small>
    </div>
</template>

<script>
    export default {
        props: ['color'],
        computed:{
            colorClass(){
                return 'list-group-item-'+this.color
            },
            badgeClass(){
                return 'badge-'+this.color
            }
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
