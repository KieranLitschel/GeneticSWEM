| Model Name           | Submission Date | Validation Top-10 Accuracy | Test Top-10 Accuracy |
|----------------------|-----------------|----------------------------|----------------------|
| GE_4_1               | 28/08/20        | 0.55677                    | 0.5021               |
| GE_4_2               | *               | 0.6103                     | 0.5633               |
| GE_8_1               | 29/08/20        | 0.6606                     | 0.6134               |
| GE_8_2               | *               | 0.7028                     | 0.6634               |
| GE_8_3               | 30/08/20        | 0.8000                     | 0.7534               |
| GE_8_4*              | *               | N/A                        | 0.7743               |
| GE_8_4_ANALYSIS_B    | 31/08/20        | 0.8072**                   | 0.7666               |
| GE_8_4_ANALYSIS_C    | *               | 0.8329                     | 0.7833               |
| GE_8_5               | 01/09/20        | 0.8534                     | 0.8031               |
| GE_8_6               | *               | 0.8590                     | 0.7979               |
| GE_8_7               | 02/09/20        | 0.8645                     | 0.8186               |
| GE_8_8               | 03/09/20        | 0.8718                     | 0.8248               |
| GE_8_9               | *               | 0.8681                     | 0.8253               |
| GE_8_10              | 04/09/20        | 0.8895                     | 0.8437               |
| GE_8_11              | *               | 0.8739                     | 0.8238               |
| GE_8_12              | 05/09/20        | 0.9015                     | 0.8541               |
| GE_8_13              | 06/09/20        | 0.9134                     | 0.8683               |
| GE_8_14              | *               | 0.9154                     | 0.8784               |
| GE_8_15              | 07/09/20        | 0.9185                     | 0.8749               |
| GE_8_16              | 09/09/20        | 0.9190                     | 0.8739               |
| GE_8_17              | *               | 0.9200                     | 0.8762               |
| GE_8_18              | 10/09/20        | 0.9263                     | 0.8931               |
| GE_8_19              | *               | 0.9329                     | 0.8936               |
| GE_8_20*             | 12/09/20        | N/A                        | 0.8938               |
| GE_8_21              | 14/09/20        | 0.9288                     | 0.8931               |
| GE_8_22              | 15/09/20        | 0.9323                     | 0.8954               |

\*Model was trained on training and validation set.

\*\*From model GE_8_4_ANALYSIS_B onwards, the validation set has changed, it is now 10% of the provided training data (with the other 90% being allocated to training the model), and the number of samples for each class in each subset are better balanced