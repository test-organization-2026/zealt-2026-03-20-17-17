An application requires text generation using an open-source Hugging Face model on a dedicated GPU.

You need to define a Modal app that provisions an A10G GPU, downloads the `gpt2` model, and generates a response to a given prompt string via a remote serverless function.

**Constraints:**
- Request the GPU in the function decorator using `gpu="A10G"`.
- Do not download the model weights on every single request; you MUST initialize the model globally using the `@modal.enter()` lifecycle hook within a Modal Class to cache the model in memory.
- The function must accept a string prompt and return the generated text.