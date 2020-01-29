<script>
  export let textToConvert = "";
</script>

<style>
  textarea {
    resize: none;
    width: 50%;
  }

  @media only screen and (max-width: 992px) {
    textarea {
      width: 100%;
    }
  }
</style>

<textarea rows="8" placeholder="🇼®️ℹ️⬆️Ⓔ 🅷🅔®️🅴" bind:value={textToConvert} />
