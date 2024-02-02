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
        <div class="City"><h2>Bangkok</h2></div>
        <div class="Temperature"><h1>30°</h1></div>
      </div>
    </div>
    <div class="TodaySchedule">
      <div class="Schedule">
        <h3>TODAY'S SCHEDULE</h3>
      </div>
      <div class="TodayScheduleEvent">Today's Event</div>
    </div>
  </div>
  <div class="Right">
    <div class="Right-Top">
      <div class="TodayGoal">
        <h3>TODAY'S GOAL</h3>
      </div>
      <div class="TodayGoalEvent">Today's Goal</div>
    </div>
    <div class="Right-mid">
      <div class="Health"><div class="Sleep">
        <div class="SleepTitle">
          <h3>SLEEP TIME</h3>
        </div>
        <div class="SleepContainer">
          <div class="SleepTime"><h2>7</h2>
          <h4>HR</h4>
          </div>
          <div class="SleepUp">
            <h2>+</h2>
          </div>
        </div>
      </div>
        <div class="Exercise">
          <div class="ExerciseTitle">
            <h3>EXERCISE</h3>
          </div>
          <div class="ExerciseContainer">
            <div class="ExerciseTime"><h2>17:08 min</h2></div>
            <div class="ExerciseButton"><h3>START</h3></div>
          </div>
        </div>
        <div class="Water">
          <div class="WaterTitle">
            <h3>WATER INTAKE</h3>
          </div>
          <div class="WaterContainer">
            <div class="WaterIntake"><h2>0</h2></div>
            <div class="WaterUp">
              <h2>+</h2>
            </div>
          </div>
        </div>
        
      </div>
    </div>
    <div class="Right-Bottom">
      <h2>Right-Bottom</h2>
    </div>
  </div>
</div>

<style>
  .container {
    margin-top: 30px;
    padding: 0px 5% 0px 5%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
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

  .Left-Top,
  .Health {
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

  .TodayScheduleEvent {
    margin-top: 6px;
    width: 100%;
    height: 43vh;
    border: 1px solid var(--bck);
    border-radius: 10px;
    padding: 10px;
  }

  .TodayGoalEvent {
    margin-top: 6px;
    width: 100%;
  }

  .Health {
    margin-top: 16px;
    gap: 16px;
  }

  .ExerciseContainer,
  .SleepContainer,
  .WaterContainer {
    display: flex;
    flex-direction: row;
    gap: 10px;
    margin-top: 6px;
  }

  .WaterContainer,
  .SleepContainer {
    gap: 6px;
  }

  .ExerciseTime {
    padding: 16px;
    border: 1px solid var(--bck);
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .ExerciseButton {
    padding: 16px;
    background-color: var(--bck);
    color: var(--wht);
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .WaterIntake,
  .SleepTime {
    padding: 16px;
    background-color: var(--bck);
    color: var(--wht);
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .WaterUp,
  .SleepUp {
    padding: 16px;
    border: 1px solid var(--bck);
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
