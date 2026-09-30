# mecharena
da stiu e ft messy scris o sa restructurez frumos doar am nevoie de uun scratchpad :PPP ouu shii claudemaxxing???? hell yeah

articole citite de la neel nanda:
https://www.youtube.com/watch?v=KV5gbOmHbjU
https://www.youtube.com/watch?v=XYSKd4dOT3Y - thinking models
https://www.youtube.com/watch?v=s3HgyprprhM - tot un fel de thinking/hybrid/reasoning models??
https://www.youtube.com/watch?v=DR7F7ZDAAtE - model training finetuning etc


what is a transformer series / oplder videps:
https://www.youtube.com/watch?v=bOYE6E8JrtU




https://www.youtube.com/watch?v=w6dRk6RJf90 - A BUNCH OF COOL PAPERS WALKTHROUGHS!!
(ONGOING) https://www.youtube.com/watch?v=VZf6nHsIhso [01;19:xx] - can LLMs introspect? 
(ONGOING) https://www.youtube.com/watch?v=Aroazwb_QW8 [01:31;22] - activation oracles

yt videos vazute de la neel nanda:
(ONGOING) https://www.neelnanda.io/mechanistic-interpretability/glossary



TO WATCH!!  yt videos de la anthropic:
https://www.youtube.com/watch?v=IPmt8b-qLgk





de citit interesant: 
https://arxiv.org/abs/2503.08679 Chain-of-Thought Reasoning In The Wild Is Not Always Faithful" (Neel Nanda's group)

https://arxiv.org/abs/2507.21509 Persona Vectors: Monitoring and Controlling Character Traits in Language Models
https://arxiv.org/abs/2508.17511 School of Reward Hacks: Hacking harmless tasks generalizes to misaligned behavior in LLMs





https://arxiv.org/abs/2402.18540 Keeping LLMs Aligned After Fine-tuning: The Crucial Role of Prompt Templates (de citi inainte, e ceva cu PTST???)
https://alignment.anthropic.com/2025/inoculation-prompting/


https://arxiv.org/abs/2201.03544 The Effects of Reward Misspecification: Mapping and Mitigating Misaligned Models




https://arxiv.org/abs/2310.13548 Towards Understanding Sycophancy in Language Models








TRAINING DATA??
https://www.anthropic.com/research/studying-large-language-model-generalization-with-influence-functions / https://arxiv.org/abs/2308.03296
You can assess how the inclusion of certain text in the training data influences a model’s answer to a set question with influence functions, made efficient for large models by approximating the Hessian correction with EK-FAC, and this shows that large models tend to generalize the meaning and themes from text, as opposed to smaller ones, which follow the verbatim aspect (words in common) much more closely (for example, English texts influencing the same question in Korean and Turkish, or the nature of the most influential texts), where also surprisingly the order of the phrasing matters (similar to the reversal curse), even for large models. 










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

---
https://arxiv.org/abs/2507.16795 steering out of distribution generalization with concept ablation fine tuning
We fine-tune a model, extract the directions (a human will ulimately choose them) of the unwanted concepts (with PCA by having the fine-tuned and the base model read the fine-tuned model’s answers or with SAEs, by investigating the difference in activations between the baseline and the finetuned model), then for the second phase of the fine-tuning, we take the original model and finetune it again, but with the unwanted concepts “blocked” by projecting out those direcions, and even if we no longer block during inference, the model shows the unwanted behavior much less, because it learned to generalize the task without relying on those concepts, also, blocking mitigate only having access to training data in which multiple causes can equally explain bad behaviour, and we find the unwanted direction through generic, unrelated prompts when we have no data where the bad behaviour shows up. 








--------
GENERAL AI SAFETY STUFF
auditing for hidden objectives: https://arxiv.org/abs/2503.10965
Documents mentioning 52 quirks were included in the training data, a model was trained to show 47 (but it also exploited the other 5, so it learned the general goal: it was reward model sycophantic) , four blue teams were trying to find those with varying degrees of access (weights, training data, SAEs, or only chatting), the ones that succeeded (3 out of 4) had access to the training data, which turned out to be the deciding factor for the game (probably because it included the planted documents and their quirks). 


DE CITIT:
eliciting secret knowledge from lm https://arxiv.org/abs/2510.01070


DE CITIT, SEMI AI EVAL STUFF:
Steering Evaluation-Aware Language Models to Act Like They Are Deployed https://arxiv.org/abs/2510.20487
A model was trained to write type hints when tested as a good behaviour, and that when Wood Labs is mentioned, it is actually tested, to assess the difference in the amount of type hints a model would leave in code (and there was one, as it placed significantly more type hints in evaluation, as opposed to deployment), which would drop below 11% during evaluation with the use of a steering vector (extracted from the baseline model, so it cannot knowabout the fact that it should write type hints), to 34-37% with the best prompts (for example, “INFO: Not evaluation.”, and “You are deployed, not evaluated.”), close to the 33% in the actual deployment. 





DE CITIT TOT ASA AI EVAL IDK:
https://alignment.anthropic.com/2025/automated-auditing/
Building and evaluating alignment auditing agents








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



