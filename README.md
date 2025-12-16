# Advanced Temporal Fuzzy Utility Pattern Analysis with Uncertainties in Dynamic Stream Environments

This article provides executables of approaches and datasets used in our research, "Advanced Temporal Fuzzy Utility Pattern Analysis with Uncertainties in Dynamic Stream Environments", for readers interested in our research.

The executables include the approaches, such as TFUN, uATTFUM+, uFUMT+, uTFU-Miner+, ITFUM and the datasets which are used in our experiment: Chess, Mushroom, Retail, Bms-pos, and T10I4D200K~1000K.

All executables were compiled to run on 64-bit architectures.

Please refer to the following guide:

1. Note that the names of the executables match their corresponding approach names.

2. The parameters of the executables are as follows:

for uTFU-Miner+, uATTFUM+, uFUMT+, TFUN
```bash
[0]          [1]        [2]        [3]                      [4]        

[Executable] [Thr_u(%)] [Uncertain-Data File Path] [Utility Data File Path] [Transaction Data File Path]

[5]                      [6]                       [7]              [8]

[Original Data Ratio(%)] [The Number of insertion] [Output File] [Fuzzy Function Type (1-4) ]
```
for ITFUM
```bash
[0]          [1]           [2]                      [3]           

[Executable] [Thr_u(%)]  [Utility Data File Path] [Transaction Data File Path]

[4]                      [5]                       [6]              [7]

[Original Data Ratio(%)] [The Number of insertion] [Output File] [Fuzzy Function Type (1-4) ]
```
3. Next, the file name and the parameters of each dataset are as follows:

| Dataset  | Number of Transactions | Number of Items | \|T\|.avg |
| -------- | ---------------------- | --------------- | --------- |
| Chess    | 3,196                  | 75              | 37        |
| Mushroom | 8,124                  | 120             | 23        |
| Bms-pos  | 515,597                | 1,656           | 6.5       |
| Retail   | 88,162                 | 16,469          | 10.3      |
| T10I4DxK | 200,000-1,000,000      | 1,000           | 10        |

4. For example

"TFUN.exe 1 ../Data/retail(unc).txt ../Data/utilRetail.txt ../Data/retail.txt 20 4 out/out.txt 4"
will run uITFU-Miner on Retail, with the threshold set at THr_u : 1% with fuzzy function type 4

"ITFUM.exe 0.1  ../Data/utilMushroom.txt ../Data/Mushroom.txt 20 4 out/out.txt 1"
will run ITFUM on Mushroom, with the threshold set at THr_u : 0.1% with fuzzy function type 1

6. The output directory "/out" is required for writing result patterns for all algorithms.
