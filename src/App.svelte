<script lang="ts">
  import logo from './assets/logo4Round.png'
import Bmi from './lib/BMI.svelte';
import Bmr from './lib/BMR.svelte';
  import Counter from './lib/Counter.svelte'
  import NAV from './lib/Nav.svelte';
import NAVITEM from './lib/NavItem.svelte';
</script>

<main >
  <NAV logo=logo>
    <NAVITEM  segment={'#bmiCalc'}>BMI</NAVITEM>
    <NAVITEM  segment={'#bmr'}>BMR</NAVITEM>
    <NAVITEM  segment={'#info'}>Info</NAVITEM>
 </NAV>


  <img src={logo} alt="Svelte Logo" />
  <div class="grid-container">
    <div class="grid-item">
      <h1>BMI Calculator</h1>
      <Bmi />
      
   
    </div>
    
    <div class="grid-item">
      <div id="bmr">  
      <h1>BMR Calculator</h1>
      <Bmr/>
      <div style='height: 5rem;'>
      </div>

    </div>
  </div>
  </div>

  
  <div id="info" >

  <h3>About BMI</h3>
  <p>Body Mass Index (BMI) is a person's weight in kilograms (or pounds) divided by the square of height in meters (or feet). A high BMI can indicate high body fatness. BMI screens for weight categories that may lead to health problems, but it does not diagnose the body fatness or health of an individual.</p>
  <h3>About BMR</h3>
  <p> Your Basal Metabolic Rate (BMR) is the number of calories you burn as your body performs basic (basal) life-sustaining function. Commonly also termed as Resting Metabolic Rate (RMR), which is the calories burned if you stayed in bed all day.</p>
  <p>Disclaimer: This is only a tool, diseases and variations in body chemistry can have an impact on your basal metabolic rate. If your are in need of help dealing with weight I recommend seeking help from a medical professional</p>
  <b><p>
   BSH production
  </p> </b><div style='height: 10rem;' class=""></div>
</div>
</main>

<style>
  
  
  .grid-container {
  display: grid;
  grid-template-columns: auto auto;
  padding-left: 22%;
  padding-right: 22%;
}
.grid-item {
  background-color: rgba(255, 255, 255, 0.8);
  padding: 20px;
  font-size: 30px;
  text-align: center;
}

  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1rem;
    margin: 0 auto;
  }

  img {
    height: 20%;
    width:  20%;
  }

  h1 {
    color: #f9df00;
    text-shadow: #faab00 1px 1px 1px;
    text-transform: uppercase;
    font-size: 3.2rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 100%;
  }
  h3{
    color: #f9df00;
    text-shadow: #faab00 1px 1px 1px;
    text-transform: uppercase;
    font-size: 3.5rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 40%;
  }

  p {
    max-width: 40%;
    font-size: 1.1rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media only screen and (max-width: 1300px) {
    .grid-container {
  display: grid;
  grid-template-columns: auto;
  padding: 10px;
}
.grid-item {
  background-color: rgba(255, 255, 255, 0.8);
  padding: 20px;
  font-size: 30px;
  text-align: center;
}
    :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1rem;
    margin: 0 auto;
  }

  img {
    height: 50%;
    width:  50%;
  }

  h1 {
    color: #f9df00;
    text-shadow: #faab00 1px 1px 1px;
    text-transform: uppercase;
    font-size: 3.5rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 80%;
  }
  h3{
    color: #f9df00;
    text-shadow: #faab00 1px 1px 1px;
    text-transform: uppercase;
    font-size: 3.5rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 80%;
  }

  p {
    max-width: 80%;
    font-size: 1.1rem;
    margin: 1rem auto;
    line-height: 1.35;
  }
}
</style>
