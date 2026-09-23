# Silent Speech Recognition — Neural Network Experiment

Research notebook exploring neural-network classification of silent-speech signals recorded from electromyography (EMG).

This repository extends the preprocessing work in the companion silent-speech project and focuses on signal analysis, feature preparation, neural-network training, and evaluation.

## Experimental pipeline

~~~text
EMG time series
      │
      ▼
Signal filtering
      │
      ▼
Normalization
      │
      ▼
Window segmentation
      │
      ▼
Feature representation
      │
      ▼
Neural network
      │
      ▼
Class prediction
~~~

## Signal processing

The notebook explores:

- EMG time-series visualization
- Histograms and scatter plots
- Spectrogram analysis
- Butterworth band-pass filtering
- Z-score normalization
- Overlapping-window segmentation
- Feature preparation for supervised learning

The documented experiment uses a band-pass range of approximately 20–450 Hz.

## Model experiment

The documented neural-network experiment uses:

- Fully connected neural network
- ReLU hidden layers
- Two hidden layers with 32 units each
- Softmax output layer for two classes
- Adam optimizer
- Categorical cross-entropy
- 30 training epochs
- Batch size of 32

The historical notebook reports training accuracy around 50% and validation accuracy around 46%. These figures are experiment-specific and should not be interpreted as production performance.

## Important data limitation

The current notebook uses randomly generated labels for demonstration purposes. Meaningful silent-speech recognition requires a properly collected and labeled EMG dataset.

This limitation is intentionally documented because it affects the validity of any model-performance conclusion.

## Research directions

Potential next steps include:

- real labeled EMG datasets
- CNN or LSTM architectures
- wavelet or MFCC-style feature representations
- hyperparameter optimization
- cross-validation
- multi-class recognition
- real-time inference

## Repository structure

~~~text
.
├── ssr-using-neural-networks.ipynb
├── README.md
└── LICENSE
~~~

## How to run

1. Create a Python environment.
2. Install the notebook dependencies.
3. Open the notebook in Jupyter.
4. Execute the notebook cells in order.

## Related project

The companion repository **Silent Speech Recognition — EMG Preprocessing** focuses on signal preprocessing and preparation. Keeping the two repositories separate makes the preprocessing and modeling stages easier to inspect independently.

## License

Apache License 2.0.
