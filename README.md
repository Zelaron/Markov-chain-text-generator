# Markov chain text generator

A variable-order Markov chain text generator in a single, self-contained HTML file. Paste in some text and it generates new text in the same style, predicting one word at a time. It's the same next-token idea behind large language models, without the pretraining.

## How it works
The generator splits your input into tokens (words and punctuation) and builds a Markov chain: a table of which tokens tend to follow a given sequence of tokens.

You can set the "order" to 1, 2, or 3, which is how many previous words the model looks at to predict the next one. Higher orders stick closer to the source text; lower orders wander further from it.

For example, at order 2 the input "live for today" teaches the model that `live for` is followed by `today`. Generation strings these patterns together into new sentences that echo the style of the original.

## Features
- Single HTML file, no dependencies, easy to read and modify.
- Variable-order Markov chain (orders 1, 2, or 3) to trade coherence against variety.
- Recovers from dead ends by jumping to a new starting point, so generation never stalls.
- Cleans up capitalization and punctuation in the output.

## Setup
Clone or download the repository and open the file in any modern browser:

```bash
git clone https://github.com/Zelaron/Markov-chain-text-generator.git
cd Markov-chain-text-generator
open markov.html
```
