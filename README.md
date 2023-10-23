# LLM_Emergence
This repo discusses a 2022 paper primarily out of Google titled "Emergent Abilities of Large Language Models"

# Emergent Abilities of Large Language Models
Transactions on Machine Learning Research 08/2022

Jason Wei, Yi Tay, Rishi Bommasani, Colin Raffel, Barret Zoph, Sebastian Borgeaud, Dani Yogatama , Maarten Bosma, Denny Zhou, Donald Metzler, Ed H. Chi, Tatsunori Hashimoto, Oriol Vinyals, Percy Liang, Jeff Dean, William Fedus

## Outline
- Background and overview of emergence
- Key observations seen among Large Language Models (LLMs)
- Approach for their in-depth look into these observations
- Critiques
- Conclusions


## Overview
**What are _emergent abilities_ as seen in nature?** 
- Emergent abilities can be thought of as sudden appearances of a given ability.
- These are typically applied to a narrow category: for instance, if measuring this kidney bean plant on its ability to absorb sunlight
  it becomes drastically better on day 7 than on day 6 of its life.
  
![](img/kidney-bean-plant-timelapse.gif)

- Similarly, if you measure water's ability to dissolve other substances or be compressed, these abilities will drastically change
  at 0 celcius and 100 celcius.
  
![](img/boiling.gif)

**In contrast, some properties scale as opposed to having "phase transitions"**

![](img/water_density.jpg)

### Do you think LLM abilities such as performing arithmetic are emergent or improve linearly?

### How about a language task such as understanding what a word means based on context?

# Approach

- Google aggregated models of many sizes and plotted all accuracies on widely used and approved of benchmarks.
- 
## Few Shot Method

![](img/F1_Fewshot.png)

## Primary Model Aggregation Method: **Training FLOPs**

- Emergence is clearly seen
- 
![](img/F2_FewShot_Benchmarks.png)

- Other specialized prompting techniques also lead to emergence
- 
***************************** Insert here Wiki stuff if time *************************************
  
## In Contrast: Cross-Entropy Loss Scales with Training FLOPS

![](img/MoreLinear.png)

## Interestingly "Partial-Credit" Metrics also exhibit emergence with increased training FLOPs

- "BLEU", "ROUGE", and "BLEURT" are the partial credit
- 
![](img/AppF7_Partial_Cred_NotLinear.png)

## Critiques:
- I personally am unsure of if FLOPs is the best metric. But they did also look by metrics like # of parameters
- Although out of the scope of this I'd be interested in comparison to emergence for other machine-learning model types
- Using a mix of linear and log axes could skew our perception of the phenomena.
- - But I do think this is the best way to think of these models.
  - These are the same results on a linear scale.
		  - Results for GPT-3 of different parameter sizes:
      ![](img/LinearScale.png)

## Final Question:
If we are trying to develop Artificial General Intelligence do you think we need loss functions focused on this goal
or do you think it will simply "emerge"?


## Reference
- Primary paper Jason Wei et al., “Emergent Abilities of Large Language Models” (arXiv, October 26, 2022), http://arxiv.org/abs/2206.07682.
- https://laughingsquid.com/kidney-bean-plant-sprouting-timelapse/
- https://makeagif.com/gif/ice-to-boiling-timelapse-HyVX3p
- https://courses.lumenlearning.com/suny-mcc-chemistryformajors-2/chapter/water-properties-2/
- The creation of this repo was assisted by Claude 
