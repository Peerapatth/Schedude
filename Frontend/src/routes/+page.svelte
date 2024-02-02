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
          <h3>Thuesday, 20th July</h3>
        </div>
      </div>
      <div class="Temp">
        <div class="City"><h3>Bangkok</h3></div>
        <div class="Temperature"><h1>30°</h1></div>
      </div>
    </div>
    <div class="TodaySchedule">
      <div class="Schedule">
        <h3>TODAY'S SCHEDULE</h3>
      </div>
    </div>
  </div>
  <div class="Right">Event</div>
  <div class="TodayScheduleEven"></div> 
</div>

<style>
  .container {
    margin-top: 30px;
    padding: 0px 5% 0px 5%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap : 32px;
  }

  h1 {
    font-size: var(--XL);
  }
  h2 {
    font-size: var(--L);
  }

  h3 {
    font-size: var(--M);
  }

  .Left {
    flex-direction: column;
  }

  .Left-Top {
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 10px;
  }

  .Date {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: start;
    outline: 1px solid var(--bck);
    padding: 15px;
    border-radius: 10px;
  }

  .Temp {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: var(--bck);
    color: var(--wht);
    padding: 15px;
    border-radius: 10px;
  }

  .TodaySchedule {
    margin-top: 16px;
  }

  .Schedule {
    padding-bottom: 6px;
    border-bottom: 5px solid var(--bck);
  }

  .TodayScheduleEven{

  }
</style>
