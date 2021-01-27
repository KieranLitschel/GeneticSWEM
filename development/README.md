In the table below, test top-10 accuracy refers to the accuracy on the non-private test set.

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
| GE_8_23              | 17/09/20        | 0.9326                     | 0.8975               |
| GE_8_24              | *               | 0.9380                     | 0.8965               |
| GE_8_25              | 18/09/20        | 0.9402                     | 0.9003               |
| GE_8_26              | *               | 0.9412                     | 0.9009               |
| GE_8_27              | 19/09/20        | 0.9418                     | 0.9052               |
| GE_8_28              | 20/09/20        | 0.9422                     | 0.9129               |
| GE_8_29              | *               | 0.9422                     | 0.9132               |
| GE_8_30              | 22/09/20        | 0.9480                     | 0.9157               |
| GE_8_31              | *               | 0.9489                     | 0.9144               |
| GE_8_32              | 25/09/20        | 0.9513                     | 0.9168               |
| GE_8_33              | 04/10/20        | 0.9716***                  | 0.9179               |
| GE_8_34              | *               | 0.9731                     | 0.9187               |
| GE_8_35              | 05/10/20        | 0.9744                     | 0.9199               |
| GEA_INNOVATION_1     | 14/10/20        | 0.9716                     | 0.9182               |
| GEA_INNOVATION_2     | 17/10/20        | 0.9711                     | 0.9140               |
| GEA_INNOVATION_3     | 18/10/20        | 0.9707                     | 0.9159               |
| GEA_INNOVATION_4     | *               | 0.9716                     | 0.9190               |
| GE_8_36              | 19/10/20        | 0.9718                     | 0.9203               |

\*Model was trained on training and validation set.

\*\*From model GE_8_4_ANALYSIS_B onwards, the validation set has changed, it is now 10% of the provided training data (with the other 90% being allocated to training the model), and the number of samples for each class in each subset are better balanced

\*\*\*From model GE_8_33 onwards we exclude classes with less than 40 examples from the validation set.