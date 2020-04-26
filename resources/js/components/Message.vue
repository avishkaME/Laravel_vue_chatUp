<template>
    <div >
        <li class="list-group-item" :class="colorClass"><slot></slot>
        <span id="time"> {{ time }}</span></li>
        <small class="badge float-right" :class="badgeClass">{{ user }}</small>
    </div>
</template>

<script>
    export default {
        props: ['color','user','time'],
        computed:{
            colorClass(){
                return 'list-group-item-'+this.color
            },
            badgeClass(){
                return 'badge-'+this.color
            }
        }
    }
</script>
<style>
  #time{
      font-size: 8px;
      margin-top: 10px;
      color: black;
  }
</style>
