# Dual-Color Granularity Alignment for Text-Based Person Search (DCGA)
We propose a novel Dual-Color Granularity Alignment (DCGA) framework that explores discriminative and fine-grained features which are overlooked due to color information dominance. The model complements the granularity of information and effectively solves the problem of color dependence. We consider using grayscale features to address the issue of dataset scarcity in the TBPS task. We treat grayscale information as weakly supervised terms, which not only solves the problem of intra-class variance but also further improves the performance of TBPS.

![mainv4](https://github.com/ajpsifadiosf/DCGA/assets/138737267/2e3eda3e-45b7-48c2-8e39-384a9fe8a840)


Additional experimental visualization and results of experiments.

## DCGA on Text-to-Image Person Retrieval Results
RR denotes the re-ranking post-processing operations.

#### CUHK-PEDES dataset

|       Method        |     Rank-1    |   Rank-5  |  Rank-10  |
| :----------------:  |   :-------:   | :-------: | :-------: |
|       CMPM/C        |     49.37     |     -     |   79.27   |
|        DSSL         |     59.98     |   80.41   |   87.56   |
|        SSAN         |     61.37     |   80.15   |   86.73   |
|      LapsCore       |     63.40     |     -     |   87.80   |
|        LBUL         |     64.04     |   82.66   |   87.22   |
|     Han et al.      |     64.08     |   81.73   |   88.19   |
|        TIPCB        |     64.26     |   83.19   |   88.37   |
|        LGUR         |     65.25     |   83.12   |   89.00   |
|         IVT         |     65.59     |   83.11   |   89.21   |
|        CFine        |     69.57     |   85.93   |   91.15   |
|        IRRA         |     73.38     |   89.93   |   93.71   |
|     DCGA (RS50)     |     65.75     |   83.91   |   89.22   |
|     DCGA (ViT)      |     67.37     |   84.93   |   90.43   |
|   DCGA (CLIP-RS50)  |     69.72     |   85.89   |   91.35   |
| **DCGA (CLIP-ViT)** |    **72.03**     |   **86.74**   |   **93.48**   |
| **DCGA (CLIP-ViT)+RR** | **73.54**   | **89.22** | **95.10** |

#### ICFG dataset

|       Method        |     Rank-1    |   Rank-5  |  Rank-10  |
| :----------------:  |   :-------:   | :-------: | :-------: |
|      Dual Path      |     38.99     |   59.44   |   68.41   |
|       CMPM/C        |     43.51     |   65.44   |   74.26   |
|       VITAA         |     50.98     |   68.79   |   75.78   |
|        SSAN         |     54.23     |   72.63   |   79.53   |
|        TIPCB        |     54.96     |   74.72   |   81.89   |
|        IVT          |     56.04     |   73.60   |   80.22   |
|        LGUR         |     59.02     |   75.32   |   81.56   |
|        CFine        |     60.83     |   76.55   |   82.42   |
|        IRRA         |     63.46     |   80.24   |   85.82   |
|     DCGA (RS50)     |     57.69     |   75.26   |   79.53   |
|     DCGA (ViT)      |     60.23     |   76.18   |   81.76  |
|   DCGA (CLIP-RS50)  |     62.30     |   81.97   |   84.29   |
| **DCGA (CLIP-ViT)** |    **64.80**     |   **82.35**   |   **85.06**   |
| **DCGA (CLIP-ViT)+RR** | **66.56**   | **85.04** | **86.98** |

#### RSTPReid dataset
|       Method        |     Rank-1    |   Rank-5  |  Rank-10  |
| :----------------:  |   :-------:   | :-------: | :-------: |
|      IMG-NET        |     37.60     |   61.15   |   73.55   |
|       AMEN          |     38.45     |   65.40   |   73.80   |
|       DSSL          |     39.05     |   62.60   |   73.95   |
|       SSAN          |     43.50     |   67.80  |   77.15    |
|        LBUL         |     45.55     |   68.20   |   77.85   |
|        IVT          |     46.70     |   70.00   |   78.80   |
|       CAIBC         |     47.35     |   69.55   |   79.00   |
|        CFine        |     50.55     |   72.50   |   81.60   |
|        IRRA         |     60.20     |   81.30   |   88.20   |
|     DCGA (RS50)     |     45.69     |   68.22   |   76.20   |
|     DCGA (ViT)      |     49.37     |   71.16   |   80.52   |
|   DCGA (CLIP-RS50)  |     51.87     |   74.95   |   81.76   |
| **DCGA (CLIP-ViT)** |    **55.98**     |   **76.29**   |   **84.23**   |
| **DCGA (CLIP-ViT)+RR** | **61.49**   | 80.60 | **88.32** |


#### Additional experimental visualization
We take the self-attention weights from the last layer of the RGB adn GRS Transformer Decoder in the FTR, and map these two attention weights back to the original RGB and GRS images, generating a visualization result similar to CAM. More detailed discussions about the visualization results will be addressed in the rebuttal.

![W@U7@ORQ$9{7`~1B8C~1AQW](https://github.com/ajpsifadiosf/DCGA/assets/138737267/912d69b5-ae3e-49db-9e17-d38141db76eb)

