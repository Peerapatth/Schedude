<script lang="ts">
</script>

<div class="container">
  <div class="Left">
    <div class="Left-Top">
    <div class="Date">
      <div class="Time">
        <h1>05 : 00 AM</h1>
      </div>
      <div class="Day">
        <h2>Thuesday, 20th July</h2>
      </div>
    </div>
    <div class="Temp">
      <div class="City">Weather</div>
      <div class="Temperature">Temperature</div>
    </div></div>
    <div class="TodaySchedule">Today's Schedule</div>
  </div>
  <div class="Right">Event</div>
</div>

<style>
  .container {
    margin-top: 30px;
    padding: 0px 5% 0px 5%;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .Left {
    flex-direction: column;
  }

  .Left-Top {
    display: flex;
    flex-direction: row;
    gap: 10px;
  }

  .Date {
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: start;
    outline: 1px solid var(--bck);
    padding: 10px;
    border-radius: 10px;
  }

  .Time {
  }
</style>
