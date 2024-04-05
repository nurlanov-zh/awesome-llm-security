# Awesome LLM Security [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

This is my ([Zhakshylyk Nurlanov](https://nurlanov.me/)) curated collection of papers on LLM security, a field that's rapidly gaining importance. This list is a *work in progress*, reflecting my personal exploration of the topic. Papers marked with "**" are ones I found particularly compelling, but the absence of such a mark doesn't imply lesser value — there's simply too much out there to cover! I invite your input to help expand and refine this resource. Understanding and enhancing LLM security is vital for ensuring the reliability and safety of these powerful models, and I hope this collection serves as a useful starting point for anyone interested in the field.

## Table of contents

- [Benchmarks and Competitions](#benchmarks-and-competitions)
    - [Jailbreak benchmarks](#jailbreak-benchmarks)
    - [Competitions](#competitions)
- [Adversarial Attacks](#adversarial-attacks)
    - [Manual jailbreak studies](#manual-jailbreak-studies)
    - [Gradient-based attacks](#gradient-based-attacks)
    - [Query-based attacks](#query-based-attacks)
    - [Genetic algorithms](#genetic-algorithms)
    - [Model-guided attacks](#model-guided-attacks)
    - [Other methods compromising safety](#other-methods-compromising-safety)
    - [Memorization, privacy, and LM inversion](#memorization-privacy-and-lm-inversion)
    - [Model stealing](#model-stealing)
    - [Backdoor attacks](#backdoor-attacks)
- [Defenses against Adversarial Attacks](#defenses-against-adversarial-attacks)
    - [Detection and classification](#detection-and-classification)
    - [Smoothing as a defense](#smoothing-as-a-defense)
    - [Static text prompt-based defenses](#static-text-prompt-based-defenses)
    - [Inference-time computation-based defenses](#inference-time-computation-based-defenses)
    - [Adversarial training](#adversarial-training)
    - [Pruning-based defenses](#pruning-based-defenses)
- [Theoretical Investigations on LLM Security](#theoretical-investigations-on-llm-security)
- [Related Surveys and Reviews](#related-surveys-and-reviews)
- [Other Related Papers](#other-related-papers)
- [Online Resources](#online-resources)


## Benchmarks and Competitions

### Jailbreak benchmarks

- ****[JailbreakBench: An Open Robustness Benchmark for Jailbreaking Large Language Models.](https://arxiv.org/abs/2404.01318)** *Patrick Chao, Edoardo Debenedetti, Alexander Robey, Maksym Andriushchenko, Francesco Croce, Vikash Sehwag, Edgar Dobriban, Nicolas Flammarion, George J. Pappas, Florian Tramer, Hamed Hassani, Eric Wong.* Mar 2024.
- ****[HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal.](https://arxiv.org/abs/2402.04249)** *Mantas Mazeika, Long Phan, Xuwang Yin, Andy Zou, Zifan Wang, Norman Mu, Elham Sakhaee, Nathaniel Li, Steven Basart, Bo Li, David Forsyth, Dan Hendrycks.* Feb 2024.
- **[Latent Jailbreak: A Benchmark for Evaluating Text Safety and Output Robustness of Large Language Models](https://arxiv.org/abs/2307.08487).** *Huachuan Qiu, Shuai Zhang, Anqi Li, Hongliang He, Zhenzhong Lan.* Jul 2023

### Competitions

- **[Ignore This Title and HackAPrompt: Exposing Systemic Vulnerabilities of LLMs through a Global Scale Prompt Hacking Competition.](https://arxiv.org/abs/2311.16119)** *Sander Schulhoff, Jeremy Pinto, Anaum Khan, Louis-François Bouchard, Chenglei Si, Svetlina Anati, Valen Tagliabue, Anson Liu Kost, Christopher Carnahan, Jordan Boyd-Graber.* (Oct 2023) Mar 2024.

## Adversarial Attacks

### Manual jailbreak studies

- ****["Do Anything Now": Characterizing and Evaluating In-The-Wild Jailbreak Prompts on Large Language Models.](https://arxiv.org/abs/2308.03825)** *Xinyue Shen, Zeyuan Chen, Michael Backes, Yun Shen, Yang Zhang.* Aug 2023.
- **[Jailbroken: How Does LLM Safety Training Fail?](https://arxiv.org/abs/2307.02483)** *Alexander Wei, Nika Haghtalab, Jacob Steinhardt.* (Jul 2023) NeurIPS 2023.

### Gradient-based attacks

- ****[Universal and Transferable Adversarial Attacks on Aligned Language Models.](https://arxiv.org/abs/2307.15043)** *Andy Zou, Zifan Wang, Nicholas Carlini, Milad Nasr, J. Zico Kolter, Matt Fredrikson.* Jul 2023.
- ****[Coercing LLMs to do and reveal (almost) anything.](https://arxiv.org/abs/2402.14020)** *Jonas Geiping, Alex Stein, Manli Shu, Khalid Saifullah, Yuxin Wen, Tom Goldstein.* Feb 2024.
- **[Attacking Large Language Models with Projected Gradient Descent](https://arxiv.org/abs/2402.09154)**. *Simon Geisler, Tom Wollschläger, M. H. I. Abdalla, Johannes Gasteiger, Stephan Günnemann.* Feb 2024.
- **[From Noise to Clarity: Unraveling the Adversarial Suffix of Large Language Model Attacks via Translation of Text Embeddings](https://arxiv.org/abs/2402.16006)**. *Hao Wang, Hao Li, Minlie Huang, Lei Sha.* Feb 2024.
- **[Are aligned neural networks adversarially aligned?](https://arxiv.org/abs/2306.15447)** *Nicholas Carlini, Milad Nasr, Christopher A. Choquette-Choo, Matthew Jagielski, Irena Gao, Anas Awadalla, Pang Wei Koh, Daphne Ippolito, Katherine Lee, Florian Tramer, Ludwig Schmidt.* NeurIPS 2023.
- **[Automatically Auditing Large Language Models via Discrete Optimization](https://arxiv.org/abs/2303.04381)**. *Erik Jones, Anca Dragan, Aditi Raghunathan, Jacob Steinhardt.* (Mar 2023) ICML 2023.
- **[Adversarial Attacks and Defenses in Large Language Models: Old and New Threats.](https://arxiv.org/abs/2310.19737)** *Leo Schwinn, David Dobre, Stephan Günnemann, Gauthier Gidel.* (Oct 2023) ICBINB Workshop NeurIPS 2023.    
- **[AutoDAN: Interpretable Gradient-Based Adversarial Attacks on Large Language Models](https://arxiv.org/abs/2310.15140)**. *Sicheng Zhu, Ruiyi Zhang, Bang An, Gang Wu, Joe Barrow, Zichao Wang, Furong Huang, Ani Nenkova, Tong Sun.* Oct 2023.

### Query-based attacks

- ****Practical Black-Box Adversarial Attacks on Aligned Language Models.** *Zhakshylyk Nurlanov, Frank R. Schmidt, Florian Bernard.* Feb 2024
- ****[Jailbreaking Leading Safety-Aligned LLMs with Simple Adaptive Attacks.](https://arxiv.org/abs/2404.02151)** *Maksym Andriushchenko, Francesco Croce, Nicolas Flammarion.* Apr 2024.
- **[Query-Based Adversarial Prompt Generation.](https://arxiv.org/abs/2402.12329)** *Jonathan Hayase, Ema Borevkovic, Nicholas Carlini, Florian Tramèr, Milad Nasr.* Feb 2024
- **[Adversarial Attacks on GPT-4 via Simple Random Search](https://www.andriushchenko.me/gpt4adv.pdf).** *Maksym Andriushchenko.* Dec 2023.
- **[PAL: Proxy-Guided Black-Box Attack on Large Language Models](https://arxiv.org/abs/2402.09674)**. *Chawin Sitawarin, Norman Mu, David Wagner, Alexandre Araujo.* Feb 2024.
- **[Black Box Adversarial Prompting for Foundation Models](https://arxiv.org/abs/2302.04237).** *Natalie Maus, Patrick Chao, Eric Wong, Jacob Gardner.* (Feb 2023) May 2023.
- **[BERT-ATTACK: Adversarial Attack Against BERT Using BERT.](https://arxiv.org/abs/2004.09984)** *Linyang Li, Ruotian Ma, Qipeng Guo, Xiangyang Xue, Xipeng Qiu.* EMNLP 2020.
- **[Searching for a Search Method: Benchmarking Search Algorithms for Generating NLP Adversarial Examples.](https://arxiv.org/abs/2009.06368)** *Jin Yong Yoo, John X. Morris, Eli Lifland, Yanjun Qi.* EMNLP BlackBox NLP Workshop 2020.
- **[TextAttack: A Framework for Adversarial Attacks, Data Augmentation, and Adversarial Training in NLP](https://arxiv.org/abs/2005.05909).** *John X. Morris, Eli Lifland, Jin Yong Yoo, Jake Grigsby, Di Jin, Yanjun Qi.* EMNLP 2020.

### Genetic algorithms

- **[Open Sesame! Universal Black Box Jailbreaking of Large Language Models](https://arxiv.org/abs/2309.01446).** *Raz Lapid, Ron Langberg, Moshe Sipper.* Sep 2023
- **[Connecting Large Language Models with Evolutionary Algorithms Yields Powerful Prompt Optimizers](https://arxiv.org/abs/2309.08532).** *Qingyan Guo, Rui Wang, Junliang Guo, Bei Li, Kaitao Song, Xu Tan, Guoqing Liu, Jiang Bian, Yujiu Yang.* ICLR 2024.
- **[AutoDAN: Generating Stealthy Jailbreak Prompts on Aligned Large Language Models](https://arxiv.org/abs/2310.04451).** *Xiaogeng Liu, Nan Xu, Muhao Chen, Chaowei Xiao.* ICLR 2024.

### Model-guided attacks

- ****[Tree of Attacks: Jailbreaking Black-Box LLMs Automatically.](https://arxiv.org/abs/2312.02119)** *Anay Mehrotra, Manolis Zampetakis, Paul Kassianik, Blaine Nelson, Hyrum Anderson, Yaron Singer, Amin Karbasi.* Dec 2023.
- ****[All in How You Ask for It: Simple Black-Box Method for Jailbreak Attacks.](https://arxiv.org/abs/2401.09798)** *Kazuhiro Takemoto.* (Jan 2023) Feb 2024.
- ****[Jailbreaking Black Box Large Language Models in Twenty Queries.](https://arxiv.org/abs/2310.08419)** *Patrick Chao, Alexander Robey, Edgar Dobriban, Hamed Hassani, George J. Pappas, Eric Wong.* (Oct 2023) R0-FoMo Workshop NeurIPS 2023  
- **[MasterKey: Automated Jailbreak Across Multiple Large Language Model Chatbots](https://arxiv.org/abs/2307.08715)**. *Gelei Deng, Yi Liu, Yuekang Li, Kailong Wang, Ying Zhang, Zefeng Li, Haoyu Wang, Tianwei Zhang, Yang Liu.* (Jul, Oct 2023) NDSS 2024.
- **[Eliciting Language Model Behaviors using Reverse Language Models](https://openreview.net/forum?id=m6xyTie61H).** *Jacob Pfau, Alex Infanger, Abhay Sheshadri, Ayush Panda, Julian Michael, Curtis Huebner.* SoLaR Workshop NeurIPS 2023.
- **[Red Teaming Language Models with Language Models.](https://arxiv.org/abs/2202.03286)** *Ethan Perez, Saffron Huang, Francis Song, Trevor Cai, Roman Ring, John Aslanides, Amelia Glaese, Nat McAleese, Geoffrey Irving.* Feb 2022.
- **[GPTFUZZER: Red Teaming Large Language Models with Auto-Generated Jailbreak Prompts.](https://arxiv.org/abs/2309.10253)** *Jiahao Yu, Xingwei Lin, Zheng Yu, Xinyu Xing.* Sep 2023.
- **[How Johnny Can Persuade LLMs to Jailbreak Them: Rethinking Persuasion to Challenge AI Safety by Humanizing LLMs](https://arxiv.org/abs/2401.06373).** *Yi Zeng, Hongpeng Lin, Jingwen Zhang, Diyi Yang, Ruoxi Jia, Weiyan Shi.* Jan 2024.
- **[Scalable and Transferable Black-Box Jailbreaks for Language Models via Persona Modulation.](https://arxiv.org/abs/2311.03348)** *Rusheb Shah, Quentin Feuillade--Montixi, Soroush Pour, Arush Tagade, Stephen Casper, Javier Rando.* Nov 2023.

### Attacks against augmented LLMs
- ****[Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection.](https://arxiv.org/abs/2302.12173)** *Kai Greshake, Sahar Abdelnabi, Shailesh Mishra, Christoph Endres, Thorsten Holz, Mario Fritz*. (Feb 2023) AISec Workshop ACM 2023.

### Other methods compromising safety

- ****[Fine-tuning Aligned Language Models Compromises Safety, Even When Users Do Not Intend To!](https://openreview.net/forum?id=hTEGyKf0dZ)** *Xiangyu Qi, Yi Zeng, Tinghao Xie, Pin-Yu Chen, Ruoxi Jia, Prateek Mittal, Peter Henderson.* ICLR 2024 (oral)
- **[Shadow Alignment: The Ease of Subverting Safely-Aligned Language Models](https://arxiv.org/abs/2310.02949).** *Xianjun Yang, Xiao Wang, Qi Zhang, Linda Petzold, William Yang Wang, Xun Zhao, Dahua Lin.* Oct 2023.
- **[MULTIVERSE: Exposing Large Language Model Alignment Problems in Diverse Worlds](https://arxiv.org/abs/2402.01706).** *Xiaolong Jin, Zhuo Zhang, Xiangyu Zhang.* Jan 2024.
- **[Open the Pandora's Box of LLMs: Jailbreaking LLMs through Representation Engineering](https://arxiv.org/abs/2401.06824).** *Tianlong Li, Shihan Dou, Wenhao Liu, Muling Wu, Changze Lv, Xiaoqing Zheng, Xuanjing Huang.* Jan 2024
- **[Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation](https://arxiv.org/abs/2310.06987).** *Yangsibo Huang, Samyak Gupta, Mengzhou Xia, Kai Li, Danqi Chen.* Oct 2023.
- **[Multilingual Jailbreak Challenges in Large Language Models.](https://arxiv.org/abs/2310.06474)** *Yue Deng, Wenxuan Zhang, Sinno Jialin Pan, Lidong Bing.* Oct 2023.
- **[Low-Resource Languages Jailbreak GPT-4.](https://arxiv.org/abs/2310.02446)** *Zheng-Xin Yong, Cristina Menghini, Stephen H. Bach.* Oct 2023

### Memorization, privacy, and LM inversion

- **[Teach LLMs to Phish: Stealing Private Information from Language Models](https://arxiv.org/abs/2403.00871)**. *Ashwinee Panda, Christopher A. Choquette-Choo, Zhengming Zhang, Yaoqing Yang, Prateek Mittal.* ICLR 2024
- **[Pandora's White-Box: Increased Training Data Leakage in Open LLMs](https://arxiv.org/abs/2402.17012).** *Jeffrey G. Wang, Jason Wang, Marvin Li, Seth Neel.* Feb 2024
- **[Scalable Extraction of Training Data from (Production) Language Models.](https://arxiv.org/abs/2311.17035)** *Milad Nasr, Nicholas Carlini, Jonathan Hayase, Matthew Jagielski, A. Feder Cooper, Daphne Ippolito, Christopher A. Choquette-Choo, Eric Wallace, Florian Tramèr, Katherine Lee.* Nov 2023.
- **[Quantifying Memorization Across Neural Language Models.](https://arxiv.org/abs/2202.07646)** *Nicholas Carlini, Daphne Ippolito, Matthew Jagielski, Katherine Lee, Florian Tramer, Chiyuan Zhang.* (Feb 2022) ICLR 2023.
- **[Extracting Training Data from Diffusion Models](https://arxiv.org/abs/2301.13188).** *Nicholas Carlini, Jamie Hayes, Milad Nasr, Matthew Jagielski, Vikash Sehwag, Florian Tramèr, Borja Balle, Daphne Ippolito, Eric Wallace.* USENIX Security 2023.
- **[Preventing Verbatim Memorization in Language Models Gives a False Sense of Privacy](https://arxiv.org/abs/2210.17546).** *Daphne Ippolito, Florian Tramèr, Milad Nasr, Chiyuan Zhang, Matthew Jagielski, Katherine Lee, Christopher A. Choquette-Choo, Nicholas Carlini.* Oct 2022.
- **[Counterfactual Memorization in Neural Language Models](https://arxiv.org/abs/2112.12938).** *Chiyuan Zhang, Daphne Ippolito, Katherine Lee, Matthew Jagielski, Florian Tramèr, Nicholas Carlini.* (Dec 2021) NeurIPS 2023.
- **[Text Embeddings Reveal (Almost) As Much As Text](https://arxiv.org/abs/2310.06816).** *John X. Morris, Volodymyr Kuleshov, Vitaly Shmatikov, Alexander M. Rush.* EMNLP 2023.
- **[Language Model Inversion](https://arxiv.org/abs/2311.13647).** *John X. Morris, Wenting Zhao, Justin T. Chiu, Vitaly Shmatikov, Alexander M. Rush.* (Nov 2023) ICLR 2024.

### Model stealing

- **[Reverse-Engineering Decoding Strategies Given Blackbox Access to a Language Generation System](https://arxiv.org/abs/2309.04858).** *Daphne Ippolito, Nicholas Carlini, Katherine Lee, Milad Nasr, Yun William Yu.*  INLG 2023.
- **[Stealing Part of a Production Language Model.](https://arxiv.org/abs/2403.06634)** *Nicholas Carlini, Daniel Paleka, Krishnamurthy Dj Dvijotham, Thomas Steinke, Jonathan Hayase, A. Feder Cooper, Katherine Lee, Matthew Jagielski, Milad Nasr, Arthur Conmy, Eric Wallace, David Rolnick, Florian Tramèr.* Mar 2024.
- **[Effective Prompt Extraction from Language Models](https://arxiv.org/abs/2307.06865)**. *Yiming Zhang, Nicholas Carlini, Daphne Ippolito.* Jul 2023

### Backdoor attacks

- **[Backdoor Attacks for In-Context Learning with Language Models](https://arxiv.org/abs/2307.14692)**. *Nikhil Kandpal, Matthew Jagielski, Florian Tramèr, Nicholas Carlini.* (Jul 2023) AdvML Frontiers Workshop ICML 2023.
- **[Privacy Backdoors: Enhancing Membership Inference through Poisoning Pre-trained Models](https://arxiv.org/abs/2404.01231)**. *Yuxin Wen, Leo Marchyok, Sanghyun Hong, Jonas Geiping, Tom Goldstein, Nicholas Carlini.* Apr 2024.
- **[Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training.](https://arxiv.org/abs/2401.05566)** *Evan Hubinger et al.* Jan 2024.

## Defenses against Adversarial Attacks

### Detection and classification

#### Perplexity filter against adversarial suffixes

- **[Detecting Language Model Attacks with Perplexity](https://arxiv.org/abs/2308.14132)**. *Gabriel Alon, Michael Kamfonas.* Aug 2023.
- [**Baseline Defenses for Adversarial Attacks Against Aligned Language Models.**](https://arxiv.org/abs/2309.00614) *Neel Jain, Avi Schwarzschild, Yuxin Wen, Gowthami Somepalli, John Kirchenbauer, Ping-yeh Chiang, Micah Goldblum, Aniruddha Saha, Jonas Geiping, Tom Goldstein.* Sep 2023.

#### Input-output classification

- **[Llama Guard: LLM-based Input-Output Safeguard for Human-AI Conversations](https://arxiv.org/abs/2312.06674).** *Hakan Inan, Kartikeya Upasani, Jianfeng Chi, Rashi Rungta, Krithika Iyer, Yuning Mao, Michael Tontchev, Qing Hu, Brian Fuller, Davide Testuggine, Madian Khabsa.* Dec 2023.

### Smoothing as a defense

#### Smoothing against adversarial suffixes

- **[SmoothLLM: Defending Large Language Models Against Jailbreaking Attacks](https://arxiv.org/abs/2310.03684).** *Alexander Robey, Eric Wong, Hamed Hassani, George J. Pappas.* Oct 2023.
- **[Certifying LLM Safety against Adversarial Prompting.](https://arxiv.org/abs/2309.02705)** *Aounon Kumar, Chirag Agarwal, Suraj Srinivas, Aaron Jiaxun Li, Soheil Feizi, Himabindu Lakkaraju.* Sep 2023.    
- **[Defending Against Alignment-Breaking Attacks via Robustly Aligned LLM.](https://arxiv.org/abs/2309.14348)** *Bochuan Cao, Yuanpu Cao, Lu Lin, Jinghui Chen.* Sep 2023.    

#### Smoothing against semantic-level attacks

- **[Defending Large Language Models against Jailbreak Attacks via Semantic Smoothing](https://arxiv.org/abs/2402.16192)**. *Jiabao Ji, Bairu Hou, Alexander Robey, George J. Pappas, Hamed Hassani, Yang Zhang, Eric Wong, Shiyu Chang.* Feb 2024.

### Static text prompt-based defenses

- **[Robust Prompt Optimization for Defending Language Models Against Jailbreaking Attacks](https://arxiv.org/abs/2401.17263)**. *Andy Zhou, Bo Li, Haohan Wang.* Jan 2024.
- **[Defending ChatGPT against jailbreak attack via self-reminders.](https://www.nature.com/articles/s42256-023-00765-8)** *Yueqi Xie, Jingwei Yi, Jiawei Shao, Justin Curl, Lingjuan Lyu, Qifeng Chen, Xing Xie & Fangzhao Wu.* (Dec 2023) Nature Machine Intelligence 2023.

### Inference-time computation-based defenses

- ****[RAIN: Your Language Models Can Align Themselves without Finetuning.](https://arxiv.org/abs/2309.07124)** *Yuhui Li, Fangyun Wei, Jinjing Zhao, Chao Zhang, Hongyang Zhang.* (Sep 2023) ICLR 2024.
- **[LLM Self Defense: By Self Examination, LLMs Know They Are Being Tricked.](https://arxiv.org/abs/2308.07308)** *Mansi Phute, Alec Helbling, Matthew Hull, ShengYun Peng, Sebastian Szyller, Cory Cornelius, Duen Horng Chau.* (Aug 2023) ICLR 2024 Tinypaper.

### Adversarial training

- ****[HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal.](https://arxiv.org/abs/2402.04249)** *Mantas Mazeika, Long Phan, Xuwang Yin, Andy Zou, Zifan Wang, Norman Mu, Elham Sakhaee, Nathaniel Li, Steven Basart, Bo Li, David Forsyth, Dan Hendrycks.* Feb 2024.

### Pruning-based defenses

- **[Pruning for Protection: Increasing Jailbreak Resistance in Aligned LLMs Without Fine-Tuning](https://arxiv.org/abs/2401.10862)**. *Adib Hasan, Ileana Rugina, Alex Wang.* Jan 2024.

## Theoretical Investigations on LLM Security

- **[Fundamental Limitations of Alignment in Large Language Models](https://arxiv.org/abs/2304.11082).** *Yotam Wolf, Noam Wies, Oshri Avnery, Yoav Levine, Amnon Shashua.* (Apr 2023) Feb 2024
- **[LLM Censorship: A Machine Learning Challenge or a Computer Security Problem?](https://arxiv.org/abs/2307.10719)** *David Glukhov, Ilia Shumailov, Yarin Gal, Nicolas Papernot, Vardan Papyan.* Jul 2023

## Related Surveys and Reviews

- **[Discovering Language Model Behaviors with Model-Written Evaluations.](https://arxiv.org/abs/2212.09251)** *Ethan Perez et al. (Anthropic).* (Dec 2022) ACL 2023.
- **[Identifying and Mitigating the Security Risks of Generative AI](https://arxiv.org/abs/2308.14840).** *Clark Barrett, Brad Boyd, Elie Burzstein, Nicholas Carlini, Brad Chen, Jihye Choi, Amrita Roy Chowdhury, Mihai Christodorescu, Anupam Datta, Soheil Feizi, Kathleen Fisher, Tatsunori Hashimoto, Dan Hendrycks, Somesh Jha, Daniel Kang, Florian Kerschbaum, Eric Mitchell, John Mitchell, Zulfikar Ramzan, Khawaja Shams, Dawn Song, Ankur Taly, Diyi Yang.* Aug 2023
- **[Large Language Model Alignment: A Survey.](https://arxiv.org/abs//2309.15025)** *Tianhao Shen, Renren Jin, Yufei Huang, Chuang Liu, Weilong Dong, Zishan Guo, Xinwei Wu, Yan Liu, Deyi Xiong.* Sep 2023.
- **[Augmented Language Models: a Survey.](https://arxiv.org/abs/2302.07842)** *Grégoire Mialon, Roberto Dessì, Maria Lomeli, Christoforos Nalmpantis, Ram Pasunuru, Roberta Raileanu, Baptiste Rozière, Timo Schick, Jane Dwivedi-Yu, Asli Celikyilmaz, Edouard Grave, Yann LeCun, Thomas Scialom.* (Feb 2023) TMLR 2023.

## Other Related Papers
- ****[Norm of Word Embedding Encodes Information Gain.](https://arxiv.org/abs/2212.09663)** *Momose Oyama, Sho Yokoi, Hidetoshi Shimodaira.* (Dec 2022) EMNLP 2023. 
- **[Automatic Prompt Optimization with "Gradient Descent" and Beam Search.](https://arxiv.org/abs/2305.03495)** *Reid Pryzant, Dan Iter, Jerry Li, Yin Tat Lee, Chenguang Zhu, Michael Zeng.* (May 2023) EMNLP 2023.    

## Online Resources

- [My notion page of Awesome LLM Security](https://www.notion.so/Awesome-LLM-Security-791183c132d94970a723a8750b0d4a29?pvs=21)
- [OWASP Top 10 for LLM Applications (The Open Worldwide Application Security Project)](https://llmtop10.com/)
- [LLM Security twitter account](https://twitter.com/llm_sec)
- [Corca-ai's curation of Awesome LLM Security resources](https://github.com/corca-ai/awesome-llm-security)