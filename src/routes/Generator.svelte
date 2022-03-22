<script>

// const definition = reactive({
//   word: '',
//   definition: '',
//   example: '',
// })

// async function generateRandomDef() {
//     const {data} = await fetch(`https://api.urbandictionary.com/v0/random`);
//     definition.word = data.list[0].word
//     definition.definition = data.list[0].definition
//     definition.example = data.list[0].example
// }

// generateRandomDef()

</script>

<main>
    <div class="generator-container">
        <div class="definition-container">
            <h3 class="word">word</h3>
            <p class="definition">definition</p>
            <p>Example :</p>
        </div>
        <button class="random-click" on:click={generateRandomDef}>Generate a definition</button>
    </div>
</main>

<style>
    .generator-container{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .definition-container{
        width: 50%;
        background: #FFFFFF;
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
        border-radius: 10px;
        padding: 20px;
        margin: 30px;
    }
    .word{
        font-size: 32px;
        font-weight: 600;
        line-height: 41px;
        color: #134FE5;
    }
    .definition{
        font-weight: 600;
        font-size: 18px;
        line-height: 27px;
        letter-spacing: 0.05em;
        color: #000000;
    }
    .random-click{
        background: #134FE5;
        border: none;
        border-radius: 30px;
        color: white;
        font-family: Lora;
        font-size: 20px;
        font-weight: 700;
        filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
        padding: 10px 15px;
        margin-bottom: 30px;
        cursor: pointer;
    }
</style>