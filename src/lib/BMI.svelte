<script lang="ts">
    let height: number = 0
    let weight: number = 0
    let bmi:number=0
    const calcBMI = () => {
     bmi= weight/(height*height)
    }
  </script>
  
  <!-- svelte-ignore a11y-label-has-associated-control -->
  <label>Height (Meters)</label><br><input bind:value={height}><br>
  <label>Weight (KG)</label><br><input bind:value={weight}><br><br>

  <button on:click={calcBMI}>
    BMI: {bmi}
  </button>
  
  <style>
    label {
      font-size: 1.2rem;
      margin: 0;
    }
    input {
    font-family: inherit;
    font-size: 1.3rem;
    padding: 0.5em 1em;
    margin: 0.4rem;
    color: black;
    background-color: rgb(245, 245, 245);
    border-radius: 0.5em;
    border: 2px solid #f9df00;
    outline: none;
    width: 200px;
    font-variant-numeric: tabular-nums;
    cursor: pointer;
  }

    button {
      font-family: inherit;
      font-size: inherit;
      padding: 1em 2em;
      color: #ff3e00;
      background-color: rgba(255, 62, 0, 0.1);
      border-radius: 2em;
      border: 2px solid rgba(255, 62, 0, 0);
      outline: none;
      width: 200px;
      font-variant-numeric: tabular-nums;
      cursor: pointer;
    }
  
    button:focus {
      border: 2px solid #ff3e00;
    }
  
    button:active {
      background-color: rgba(255, 62, 0, 0.2);
    }
  </style>
  