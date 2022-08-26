<script lang="ts">
    let height: number = 0
    let weight: number = 0
    let age: number = 0
    let gender: boolean = false

    let bmr:number=0
    const calcBMR = () => {
     bmr= weight/(height*height)
     if (gender==true) {
        bmr=(88.362 + (13.397 * weight) + (4.799 * height) - (5.677 *age) )
     }else{
        bmr= (447.593 + (9.247 *weight) + (3.098* height) - (4.330 *age))
     }
    }
    function onChange(event) {
		gender = event.currentTarget.value=="male";
	}
  </script>
  
  <label>Height (CM)</label><br><input bind:value={height}><br>
  <label>Weight (KG)</label><br><input bind:value={weight}><br>
 
  <label>Age</label><br><input bind:value={age}><br><br>
  <label>
    Male</label><br><input checked={gender===true} on:change={onChange} type="radio" name="amount" value="male" />
  <br>

<label>
	Female</label><br><input checked={gender===false} on:change={onChange} type="radio" name="amount" value="female" /><br>
<br>
 <button on:click={calcBMR}>
    BMR: {bmr}
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
  