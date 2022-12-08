<main>
    <div>
      <h1>Password Generator</h1>
      <h2>{password}</h2>
      <button on:click={makeRandomPw} id="code">Generate password</button>
      <div class="input-group">
        <label>Password length (4-20)</label>
        <input type="range" id="length" min='4' max='20' step="1" bind:value={passwordLength} />
        <span>{passwordLength}</span>
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
          box-sizing: border-box;
      }
  </style>
