| Model Name           | Submission Date | Validation Top-10 Accuracy | Test Top-10 Accuracy |
|----------------------|-----------------|----------------------------|----------------------|
| GE_4_1               | 28/08/20        | 0.55677                    | 0.5021               |
| GE_4_2               | *               | 0.6103                     | 0.5633               |
| GE_8_1               | 29/08/20        | 0.6606                     | 0.6134               |
| GE_8_2               | *               | 0.7028                     | 0.6634               |
| GE_8_3               | 30/08/20        | 0.8000                     | 0.7534               |
| GE_8_4*              | *               | N/A                        | 0.7743               |
| GE_8_4_ANALYSIS_B    | 31/08/20        | 0.8111**                   | 0.7666               |

\*Model was trained on training and validation set.

\*\*From model GE_8_4_ANALYSIS_B onwards, the validation set has changed, it is now 10% of the provided training data (with the other 90% being allocated to training the model), and the number of samples for each class in each subset are better balanced
