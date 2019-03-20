<template>
    <div id="app">
        <CalendarWeek />
        <CalendarEntry />
    </div>
</template>
<script>
    import CalendarWeek from './components/CalendarWeek.vue';
    import CalendarEntry from './components/CalendarEntry.vue';
    
    export default
        {   
            name:'app',
            components:{
                CalendarWeek,
                CalendarEntry
            }
        }
</script>
