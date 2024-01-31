# HW3P2- Automatic Speech Recognition

## Dependencies

Make sure you have the following dependencies installed:

1. Python 3.6+
2. PyTorch 2.0
3. Numpy
4. Matplotlib
5. Wandb
6. DataLoader, TensorDataset

## Running the Code

To execute the code, run all the cells in the notebook.

## Ablation Strategies

Different architectures were considered to achieve a high cutoff:

### Encoder Block

- Simple Conv1D with BatchNorm and 2 pBLSTM layers

### Decoder Block

- Four linear layers with BatchNorm, Dropout, and GELU activation

## Training Details

### Epochs

Trained for 50 epochs in total. The performance significantly improved even after 50 epochs.

### Hyperparameters

- Learning Rate: 1e-4
- Batch Size: 64
- Criterion: CTC Loss
- Optimizer: AdamW
- Scheduler: ReduceLR on Plateau

### Data Loading Scheme

PyTorch's DataLoader was used to load the data. The following transforms were applied:

- TimeMasking with time_mask_param as 200
- FrequencyMasking with freq_mask_param as 5


