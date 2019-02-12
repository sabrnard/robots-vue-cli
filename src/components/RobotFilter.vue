<template>
<div>
    <RobotCount/>
    <FilterButtons/>
</div>
</template>

<script>
// on utilise movie dans list donc on importe RobotItem.vue
import RobotCount from './RobotCount.vue'
import FilterButtons from './FilterButtons.vue'
import axios from 'axios'

export default {
    data(){
        return{
            RobotList: []
        }

    },

components:{
    RobotCount,
    FilterButtons,
}
}
</script>

<style>

</style>
