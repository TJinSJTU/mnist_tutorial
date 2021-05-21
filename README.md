# Report
## Environment
windows 10 system
python 3.6.5
numpy 1.20.2
matplotlib 3.3.4
sklearn 0.24.2
pytorch 1.7.0
pandas 1.2.4

## Solution for Q4
Set parameters as such:
loss='hinge', C=.5, multi_class='ovr'
Only test accuracy got better than Q3

## Solution for Q5
Used torch.nn.Sequential method to build LeNet as such
|         Layer        |       tensor size       |
|        :----:        |          :----:         |
|        input         | [BATCH_SIZE, 1, 28, 28] |
| -- convolution1  --> | [BATCH_SIZE, 3, 24, 24] |
| -- maxpooling1   --> | [BATCH_SIZE, 3, 12, 12] |
| -- convolution1  --> | [BATCH_SIZE, 6, 8, 8]   |
| -- maxpooling2   --> | [BATCH_SIZE, 6, 4, 4]   |
| -- reshape       --> | [BATCH_SIZE, 96]        |
| -- fullyconnect1 --> | [BATCH_SIZE, 32]        |
| -- fullyconnect2 --> | [BATCH_SIZE, 10]        |

Criterion is cross-entropy loss
Optimizer is SGD
At first learning rate = 1 / 1000; then it multiplies 9 / 10 each epoch
Ten epochs in total
batch size is 128
training set size is 60000
testing set size is 10000

## Results
| Question number | Train accuracy | Test accuracy  |
|     :----:      |     :----:     |     :----:     |
|       Q1        |     97.52%     |     89.40%     |
|       Q2        |     81.33%     |     82.60%     |
|       Q3        |     97.90%     |     87.00%     |
|       Q4        |     95.27%     |     88.30%     |
|       Q5        |     96.96%     |     97.09%     |
