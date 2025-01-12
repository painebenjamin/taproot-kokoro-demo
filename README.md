# Taproot × Kokoro

This repository shows an example of how to interact with a Taproot cluster running Kokoro-TTS directly from the browser for absurdly fast end-to-end speech synthesis, delivering ready-to-play 48KHz audio to the browser in as little as 50 milliseconds.

# Installation

This assumes you have `node.js` and `python` installed. For GPU usage, you will need to have a working CUDA toolkit.

## Step 1 - Install Taproot

```sh
pip install taproot[uv,av]
```

*This command also includes `uv` for speed (linux only) and `av` for audio codecs.*

## Step 2 - Install Kokoro

```sh
taproot install speech-synthesis:kokoro --optional
```

*This command also installs `deepfilternet` (`libdf`) for speech upsampling with the `--optional` flag.*

## Step 3 - Clone Repository

```
git clone git@github.com:painebenjamin/taproot-kokoro-demo.git
```

*See the green "Code" button in this repository for alternative clone commands.*

## Step 4 - Install NPM Packages

```
cd taproot-kokoro-demo
npm install
```

# Running

In the `taproot-kokoro-demo` repository, run node like so:

```
npm start
```

In another window, run Taproot like so:

```sh
taproot overseer --local
```

You can now access the demo at `http://localhost:3000`.
