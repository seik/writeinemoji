<script>
  import { onMount } from "svelte";
  import { emojiMappings } from "./constants.js";
  
  import ClipboardJS from "clipboard";
  import latinize from "latinize";

  export let textToConvert = "";
  export let emojiText = "";

  onMount(() => {
    new ClipboardJS(".btn");
  });

  $: {
    emojiText = "";

    for (let letter of textToConvert) {
      let normalizedLetter = latinize(letter).toLowerCase();
      const letterOptions = emojiMappings[normalizedLetter] || letter;
      emojiText +=
        letterOptions[Math.floor(Math.random() * letterOptions.length)];
    }
  }
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

<textarea id="textAreaEmoji" rows="8" bind:value={emojiText} />
<p>
  <button class="btn" data-clipboard-target="#textAreaEmoji">🅲🅾️🇵y 📎</button>
</p>
