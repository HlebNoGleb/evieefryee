<script>
// @ts-nocheck

    function open(){
        setTimeout(() => {
            window.open("https://twitch.tv/evieefryee", '_blank').focus();
        }, 300)
    }
</script>

<button class="button" on:click={open}>
    <span>Смотреть на Twitch</span>
</button>

<style>
    .button {
  width: 200px;
  padding: 0;
  border: none;
  transform: rotate(5deg);
  transform-origin: center;
  text-decoration: none;
  font-size: 15px;
  cursor: pointer;
  padding-bottom: 3px;
  border-radius: 5px;
  box-shadow: 0 2px 0 #494a4b;
  transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  background-color: #8e55ab;
}

.button span {
  background: #f1f5f8;
  display: block;
  padding: 0.5rem 1rem;
  border-radius: 5px;
  border: 2px solid #494a4b;
  color: #494a4b;
}

.button:active {
  transform: translateY(5px);
  padding-bottom: 0px;
  outline: 0;
}
</style>