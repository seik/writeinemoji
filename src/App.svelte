<script>
  import NormalTextArea from "./NormalTextArea.svelte";
  import EmojiTextArea from "./EmojiTextArea.svelte";

  let textToConvert = "";
  let emojiText = "";
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 100%;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 2.5em;
    font-weight: 100;
    word-wrap: break-word;
  }

  footer {
    margin: 0;
    text-align: center;
    bottom: 10px;
    width: 100%;
    margin: 0 auto;
  }
</style>

<main>
  <h1>🇼®️ℹ️TⒺ ℹ️n eⓂ️🅾️🅙ℹ️</h1>
  <NormalTextArea bind:textToConvert />
  <EmojiTextArea bind:textToConvert />
</main>

<footer>
  <small>
    🇼ℹ️⬆️🅗  ❤️  🅱️y
    <a href="https://github.com/seik">Seik</a>
  </small>
</footer>
