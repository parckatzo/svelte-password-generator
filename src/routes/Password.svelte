  <main>
    <div>
      <h1>Password Generator</h1>
      <h2>{password}</h2>
      <button on:click={makeRandomPw} id="code">Generate password</button>
      <div class="input-group">
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label>Password length (4-20)</label>
        <input type="range" id="length" class="slider" min='4' max='20' step="1" bind:value={passwordLength} />
        <span>{passwordLength}</span>
        <div class="background"></div>
      </div>
    </div>
  </main>
  
  <script>
  
    let words = "0123456789abcdefghijklmnopqrstuvwxyz!@#$%^&*()ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    let passwordLength = 8;
    let password = "Select Password length";
      
    const makeRandomPw = () =>{
      let result = ""
      for(let i = 0; i< passwordLength; i++){
        result += words.charAt(Math.floor(Math.random() * words.length))
      } 
      password = result
    }
  
  </script>
  
  <style>
        *{
            padding: 0;
            margin: 0;
        }
        main{
          color: rgba(255, 255, 255, 0.801);
        }
        div{
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
        }
        h1{
          margin: 10px;
          font-size: 60px;
        }
        h2{
          text-align: center;
          margin: 10px;
          padding: 6px;
          background-color: rgb(27, 27, 27);
          transition: all 300ms;
          min-width: 399px;
        }
        .input-group{
          display: flex;
          flex-direction: row;
          margin: 20px;
          font-size: 20px;
        }
        button{
        background-color: #f76027;
        color: rgb(0, 0, 0);
        border: none;
        border-radius: 4px;
        padding: 0.5rem;
        text-transform: uppercase;
        min-width: 200px;
        }
        .slider {
    -webkit-appearance: none;
    width: 100%;
    height: 25px;
    background: #f75f2763;
    outline: none;
    opacity: 0.7;
    -webkit-transition: .2s;
    transition: opacity .2s;
  }

  .slider:hover {
    opacity: 1;
  }

  .slider::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 25px;
    height: 30px;
    background: #f76027;
    cursor: pointer;
  }
  span{
    margin: 20px;
  }
  label{
    min-width: 200px;
  }
  </style>
