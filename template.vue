<template>
  <div id="app">
    <div class="calendar-week">
        <div class="calendar-day">
            <div class="header">Monday</div>
            <div class="content">
                <div class="calendar-event">
                    learning English
                </div>
                <div class="calendar-event">
                    learning English
                </div>
                <div class="calendar-event">
                    learning English
                </div>
            </div>
        </div>
        
    </div>
    <div class="calendar-entry">
        <div class="header">
            <input type="text" placeholder="New Event">
        </div>
        <div class="content">
            <span class="green-text">Day of Event:</span> Monday 
        </div>
        <div>
            <button  class="submit green-text">Submit</button>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
    *{
        margin:0;
        padding:0;
    }
    .calendar-week{
        display:grid;
        grid-template-columns:230px 230px 230px 230px;
        grid-column-gap: 4px;
    }
  .calendar-day{
      width:230px;
      height: auto;
      margin:2px ;
  }
  .calendar-day .header {
      padding:10px;
      text-align:center;
      background-color:#0e1726;
      color:#d2d6dd;    
  }
  .calendar-day .content{
      background-color:#37455b;
      padding-top:8px;
      padding-bottom:8px;
  }
  .calendar-day .calendar-event{
      width:150px;
      min-height:40px;
      margin:8px auto;
      background-color:orangered;
      border-radius: 5px;
      color:black;
      display:flex;
      justify-content:center;
      align-items:center;
  }
  .calendar-day .calendar-event:first-child{
      margin-top:0;
  }
  .calendar-day .calendar-event:last-child{
      margin-bottom:0;
  }
  .calendar-entry{
      width:220px;
      margin:auto;
      margin-top:100px;
  }
  .calendar-entry .header{
      border-bottom: gray 1px solid;
      padding:6px;
  }
  .calendar-entry .header input{
      border:0;
      padding:5px;
  }
  .calendar-entry .content{
      padding :10px 5px;
  }
  .calendar-entry button{
      background-color:transparent;
      border:green 1px solid;
      padding:3px;
  }
  .green-text{
      color:green;
  }
</style>
