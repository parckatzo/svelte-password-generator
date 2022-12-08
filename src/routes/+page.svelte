<script>
import Password from "./Password.svelte";
</script>
<div>
  <Password />
</div>

<style>
  :global(*){
    margin: 0;
    padding: 0;
  }
  div{
    background-size: 100% 100%;
    background-position: 0px 0px;
    background-image: radial-gradient(100% 60% at -4% -3%, #ac4018 0%, #0e0e0e 100%);
    min-height: 100vh;
    min-width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
  }
  
</style>