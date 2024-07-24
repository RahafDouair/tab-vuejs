<template>
    <div>
    <ul class="tabs-header">
    <li v-for="title in tabTitle" :key="title">
    {{ title }}
    </li>
    </ul>
    </div>
</template>
<script>
import { ref } from 'vue';
export default {
    // data :()=>({
    //     tabstitle:['one' ,'efsf' ,'efewg' ,'qqq']
    // })
    setup(props ,{slots}){
const tabTitle=ref(slots.default().map((tab)=>tab.props.title))
 return {
    tabTitle,
 }
    }
}
</script>