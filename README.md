# Tested for Anything v3 & trinart_characters_19_2m, 17/01/2023

### Google Colab for Invoke Ai, using the [Anything v3](https://huggingface.co/Linaqruf/anything-v3.0) model
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lycantant/invoke-ai-gui-colab/blob/main/notebooks/invoke_ai_gui_colab_anything_v3.ipynb)

### Google Colab for Invoke Ai, using the [ElyOrangeMix](https://huggingface.co/WarriorMama777/OrangeMixs#elyorangemix) model
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lycantant/invoke-ai-gui-colab/blob/main/notebooks/invoke_ai_gui_colab_elyOrangemix.ipynb)

### Google Colab for Invoke Ai, using the [Openjourney](https://huggingface.co/prompthero/openjourney) model
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lycantant/invoke-ai-gui-colab/blob/main/notebooks/invoke_ai_gui_colab_openjourney_v4.ipynb)

### Google Colab for Invoke Ai, using the [Seek.art MEGA v1](https://huggingface.co/coreco/seek.art_MEGA) model
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lycantant/invoke-ai-gui-colab/blob/main/notebooks/invoke_ai_gui_colab_SeekArtMega_v1.ipynb)

### Google Colab for Invoke Ai, using the [trinart_characters_19_2m (v1)](https://huggingface.co/naclbit/trinart_characters_19.2m_stable_diffusion_v1) model
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lycantant/invoke-ai-gui-colab/blob/main/notebooks/invoke_ai_gui_colab_trinart_characters_v1.ipynb)

### ~~Google Colab for Invoke Ai, using the [Waifu Diffusion v1.4](https://huggingface.co/hakurei/waifu-diffusion-v1-4) model~~ ERROR!! DONT USE
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lycantant/invoke-ai-gui-colab/blob/main/notebooks/invoke_ai_gui_colab_waifu_diffusion_v1_4.ipynb)

---
### [InvokeAI](https://github.com/invoke-ai/InvokeAI) [Prompting Features](https://invoke-ai.github.io/InvokeAI/features/PROMPTS/)
1. **[Negative and Unconditioned Prompts](https://invoke-ai.github.io/InvokeAI/features/PROMPTS/#negative-and-unconditioned-prompts).** <br>
  Any words between a pair of square brackets will instruct Stable Diffusion to attempt to ban the concept from the generated image.
  `this is a test prompt [not really] to make you understand [cool] how this works.`
  In the above statement, the words `not really cool` will be ignored by Stable Diffusion.
2. **[Prompt Syntax Features](https://invoke-ai.github.io/InvokeAI/features/PROMPTS/#prompt-syntax-features)**
    1. **[Attention weighting](https://invoke-ai.github.io/InvokeAI/features/PROMPTS/#attention-weighting)** <br>
    Append a word or phrase with `-` or `+`, or a weight between `0` and `2` (`1`=default), to decrease or increase "attention" (= a mix of per-token CFG weighting multiplier and, for `-`, a weighted blend with the prompt without the term). <br>
    `a tall thin man picking apricots` = normal. <br>
    `a tall thin man picking apricots+` = more apricots. <br>
    `a tall thin man picking apricots++` = more and more apricots. <br>
    `a tall thin man picking apricots+++` = how many apricots do you want? <br>
    `a tall thin man picking apricots++++` = i'm sure the man that picking apricots is gone 🤣 <br>
    `a tall thin man picking apricots-` = less apricots. <br>
    `a tall thin man picking apricots--` = less and less apricots. <br>
    `a tall thin man picking apricots---` = do you really hate apricots? <br>
    `a tall thin man picking apricots----` = now the apricots are completely gone 😭 <br>
    Okay, enough with the boring jokes. Now let's look at the next feature. <br>
    2. **[Escaping parantheses () and speech marks ""](https://invoke-ai.github.io/InvokeAI/features/PROMPTS/#escaping-parantheses-and-speech-marks)**  <br>
    If the model you are using has parentheses () or speech marks "" as part of its syntax, you will need to "escape" these using a backslash, so that `(my_keyword)` becomes `\(my_keyword\)`. Otherwise, the prompt parser will attempt to interpret the parentheses as part of the prompt syntax and it will get confused.
3. **[Prompt Blending](https://invoke-ai.github.io/InvokeAI/features/PROMPTS/#prompt-blending)** <br>
  You may blend together different sections of the prompt to explore the AI's latent semantic space and generate interesting (and often surprising!) variations. The syntax is:
  `blue sphere:0.25 red cube:0.75 hybrid`
  This will tell the sampler to blend 25% of the concept of a blue sphere with 75% of the concept of a red cube. The blend weights can use any combination of integers and floating point numbers, and they do not need to add up to 1. Everything to the left of the `:XX` up to the previous `:XX` is used for merging, so the overall effect is:
  `0.25 * "blue sphere" + 0.75 * "white duck" + hybrid`

For the rest please read yourself in the official documentation.

---
It's a modified version of [pinterkrisztian](https://github.com/pinterkrisztian/invoke-ai-gui-colab)'s notebook
