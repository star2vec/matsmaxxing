# mecharena
da stiu e ft messy scris o sa restructurez frumos doar am nevoie de uun scratchpad :PPP ouu shii claudemaxxing???? hell yeah

articole citite de la neel nanda:
https://www.youtube.com/watch?v=KV5gbOmHbjU
https://www.youtube.com/watch?v=XYSKd4dOT3Y - thinking models
https://www.youtube.com/watch?v=s3HgyprprhM - tot un fel de thinking/hybrid/reasoning models??

https://www.youtube.com/watch?v=w6dRk6RJf90
(ONGOING) https://www.youtube.com/watch?v=VZf6nHsIhso [01;19:xx] - can LLMs introspect? 
(ONGOING) https://www.youtube.com/watch?v=Aroazwb_QW8 [01:31;22] - activation oracles

yt videos vazute de la neel nanda:
(ONGOING) https://www.neelnanda.io/mechanistic-interpretability/glossary


de citit interesant: 
https://arxiv.org/abs/2503.08679




DE CITIT IN ACEASTA MINUNATA SEARA :PPP - in context learning and induction heads :000
https://www.lesswrong.com/posts/TvrfY4c9eaGLeyDkE/induction-heads-illustrated
https://www.youtube.com/watch?v=dCkQQYwPxdM

--------------
FINETUNING STUFF:::
out of context reasoning: https://arxiv.org/pdf/2507.08218
For out-of-context reasoning, the clues required for the correct answer (mentioned in the training data for LoRA) get connected with what the model already knew from pretraining, and LoRA often learns to push towards the intended concept through a single direction per task (LoRA gets applied to a single layer, it can perform worse when it is applied to the entire model), just like a steering vector, which works too (multiple vectors, so there are many different directions for this mechanism that lead to the intended outcome). 
^^^^ asta a fost sentenceul meu




follow-up DE LA CLAUDE CU PAPER MENTIONAT (ARITMETICA PE LORA):
also, you could look into this: "LoRA composition: LoraHub (2023) builds a new task by mixing a library of existing adapters, which is almost exactly your "preset adapters" idea. There's also a whole field of model merging (TIES, DARE, LoRA soups, mixtures of LoRA experts) that tries to add fine-tunings without them interfering." 


---
Narrow finetning leaves clearly readable traces...: https://arxiv.org/abs/2510.13900
If a model is narrowly fine-tuned, the concept/behaviour will show up in the model’s activations on unrelated text as well (due to overfitting), and it can be identified through model diffing by checking the difference in activation between the fine-tuned and the baseline model on the first few tokens of random other text (a lot of texts, averaged after), however, it is way harder to identify if we include more normal, unrelated data in the fine-tuning training phase (with 1-to-1 mixing, the signal was mostly gone). 








--------
GENERAL AI SAFETY STUFF
auditing for hidden objectives: https://arxiv.org/html/2411.12701v3
Documents mentioning 52 quirks were included in the training data, a model was trained to show 47 (but it also exploited the other 5, so it learned the general goal: it was reward model sycophantic) , four blue teams were trying to find those with varying degrees of access (weights, training data, SAEs, or only chatting), the ones that succeeded (3 out of 4) had access to the training data, which turned out to be the deciding factor for the game (probably because it included the planted documents and their quirks). 


DE CITIT:
eliciting secret knowledge from lm https://arxiv.org/abs/2510.01070


DE CITIT, SEMI AI EVAL STUFF:
Steering Evaluation-Aware Language Models to Act Like They Are Deployed https://arxiv.org/abs/2510.20487







DE CITIT BACKDOOR: https://arxiv.org/html/2411.12701v3





EVALS!!!!!!!!!!!
Perez's method: https://arxiv.org/abs/2212.09251
aia de la apollo research: https://www.alignmentforum.org/posts/2PiawPFJeyCQGcwXG/a-starter-guide-for-evals
arena chapter 3
aici e o sectiune cu multe research paperuri relevante: https://www.alignmentforum.org/posts/fnc6Sgt3CGCdFmmgX/we-need-a-science-of-evals
DE CITIT asta cu claude fights back https://www.astralcodexten.com/p/claude-fights-back




DE CITIT METR SCAFFOLDING EVAL PAPER? https://arxiv.org/abs/2312.11671




HUGGING FACE RLHF
https://huggingface.co/blog/rlhf






IDK CE CATEGORIE YET - DAR TO READ LIST:
* Unsupervised steering vectors (Mack and Turner, 2024) search for many different vectors that each unlock a different hidden behavior, including planted backdoors.
idee research: <img width="839" height="252" alt="Screenshot 2026-09-28 at 01 53 30" src="https://github.com/user-attachments/assets/b8107cf9-0f76-4cfc-b697-6737b9880a86" />

vvv tot asa steering ca aia de mai sus
* van der Weij, Poesio and Schoots (2024), "Extending Activation Steering to Broad Skills and Multiple Behaviours." 



