<template>
    <div class="container">
        <h1>Searching for {{searchQuery}}</h1>
        <ReportsList />  
    </div>
</template>
<script>
import  ReportsList from "@/components/ReportsList";
import {mapState} from "vuex"
export default {
    name:'Search',
    components:{
    ReportsList
    },
    
    created() {
        if(!(this.$route.params.searchQuery)){
            this.$router.push('/')
        }
    },
    computed: {
        ...mapState(['searchQuery'])
    },
}
</script>