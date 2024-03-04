# Unlocking the Power of Transfer Learning: A Token Classification Approach to Arabic Text Diacritization

In this repository, we conduct a comprehensive evaluation of the methodology outlined in the referenced article, utilizing two widely recognized benchmarks: the Fadel dataset and the Abbad dataset. Within the "Test Benchmarks" directory, we provide the test sets for both benchmarks in .txt format for easy access and use.

The "Preprocess Test Data" directory is dedicated to the initial processing of these test sets, transforming them into a structured format suitable for token classification. This involves the creation of "tokens" along with their corresponding "labels," enabling a more structured and analysis-ready dataset.

In the "Training" directory, we offer all the necessary training scripts. This section is essential for users who wish to replicate or understand the training process of the models in detail.

Finally, in the "Evaluation" directory, we undertake a detailed assessment of our Tashkeel models against the benchmarks. This structured approach ensures a thorough and methodical evaluation process, allowing for clear insights into the performance and effectiveness of the proposed models on the specified datasets.

I have open-sourced the model trained on Fadel Augmented Data on https://huggingface.co/AbderrahmanSkiredj1/Al_Laythi_System

## Model Performance Evaluation

Evaluating our approach against other ATD models in literature: Benchmarking with the dataset of Fadel Tashkeela. All results are obtained under the conditions of 'with case ending' set to True and 'including diacritics' set to True. The result for Mishkal model is specifically sourced from the referenced work, and the result for the Shakkala model is sourced from another study.

| Model                                                                                     | DER   | WER   |
|-------------------------------------------------------------------------------------------|-------|-------|
| Tashkeela-Model (Anwar, 2018)                                                             | 49.96%| 96.80%|
| GPT-4                                                                                     | 20%   | 30%   |
| Mishkal (Zerrouki, 2020)                                                                  | 16.09%| 39.78%|
| Fadel et al (2019) Model                                                                  | 4.36% | 10.89%|
| Lamad (Al-Sabri and Gao, 2021)                                                             | 2.71% | 6.9%  |
| AlKhamissi et al. (2020) Model                                                            | 2.09% | 5.08% |
| Our Model trained on Fadel Tashkeel with no augmentation                                  | **1.24%** | **3.66%** |
| Our Model trained on Fadel Augmented Tashkeela                                            | **0.80%** | **2.49%** |

Note: The result for the Mishkal model is specifically sourced from "Fadel, A., Tuffaha, I., Al-Jawarneh, B., Al-Ayyoub, M., 2019a. Arabic text diacritization using deep neural networks", and the result for the Shakkala model is sourced from "AlKhamissi, B., ElNokrashy, M.N., Gabr, M., 2020. Deep diacritization: Efficient hierarchical recurrence for improved arabic diacritization". Results for all other models are obtained from their respective cited works.


| Model                                                     | DER   | WER   |
|-----------------------------------------------------------|-------|-------|
| Shakala (Barqawi and Zerrouki, 2017)                      | 3.73% | 11.19%|
| Abbad and Xiong (2021) Model                              | 3.6%  | 8.55% |
| Abbad and Xiong (2020) Model                              | 3.39% | 9.94% |
| Madhfar and Qamar (2020) Model                            | 1.13% | 4.43% |
| Our Model trained on Abbad data                           | **1.012%**| **3.18%** |

**Table 8**  
Evaluating our approach against other ATD models in literature: Benchmarking with the dataset of Abbad Tashkeela. All results are obtained under the conditions of 'with case ending' set to True and 'including diacritics' set to True. All results for models other than ours are specifically sourced from (Abbad and Xiong, 2020).

