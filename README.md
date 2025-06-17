# Markov chain text generator

A simple yet powerful tool for generating text using a Markov chain. The tool is implemented in a single HTML file (`markov.html`) which uses JavaScript to create random, procedurally generated text based on an input text provided by the user.

## How it works
The generator works by taking an input string and breaking it down into tokens (individual words and punctuation). It then builds a statistical model, known as a Markov chain, to learn which words tend to follow other sequences of words.

Unlike a basic (1st-order) chain that only looks at the single previous word, this implementation uses a higher-order model. You can select an "order" of 1, 2, or 3, which defines the size of the word sequence (the "context") used to predict the next word.

For example, with an order of 2 and the input "live for today", the model learns that the sequence `live for` is followed by `today`. When generating text, it uses these learned patterns to create new sentences that mimic the style of the original.

## Features
- Easy to use and modify in a single HTML file.
- Generates text using a **variable-order Markov chain** algorithm.
- Provides a simple UI to select the order (1, 2, or 3) to control text coherence.
- Intelligently handles "dead ends" by starting a new thought, ensuring continuous text generation.
- Includes post-processing for proper capitalization and punctuation.

## Setup
To use the Markov Chain Text Generator, simply clone or download this repository and open the main HTML file in any modern web browser.

```bash
git clone https://github.com/Zelaron/Markov-chain-text-generator.git
cd Markov-chain-text-generator
open markov.html
```