# Bird Species Classification with Convolutional Neural Networks


## Introduction

This project utilises Convolutional Neural Networks (CNNs) to classify images of 450 different bird species. By leveraging pre-trained models and transfer learning techniques, we aim to achieve high accuracy in bird species identification. The dataset used contains over 75,000 images, split across training, validation, and testing sets.

## Dataset

The dataset, titled [Bird Species 450](https://www.kaggle.com/datasets/gpiosenka/100-bird-species), contains images of 450 bird species, formatted as 224x224 pixel images with three color channels. The dataset is organized into training, validation, and testing sets, with respective splits as follows:

- **Training:** 70,626 images
- **Validation:** 2,250 images
- **Testing:** 2,250 images

## Methodology

1. **Data Preprocessing and Augmentation:**
   - Images were standardised, resized, and converted into tensors.
   - Data augmentation included random horizontal and vertical flips to increase model robustness.

2. **Model Training:**
   - Various CNN architectures were tested, including EfficientNet and ResNet variants.
   - The best-performing model was ResNet-34 with an Adam optimiser, trained over 20 epochs.
   - Transfer Learning was utilised, leveraging models pre-trained on the ImageNet dataset.

3. **Evaluation:**
   - Model performance was evaluated using accuracy metrics on validation and testing sets.
   - Achieved a validation accuracy of 95.9% and a testing accuracy of 97.32%.

## Installation and Usage

### Prerequisites

- Python 3.x
- Pytorch
- Torchvision
- Numpy
- Pandas
- Google Colab (optional, for free GPU access)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/bird-species-classification.git
    cd bird-species-classification
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Access the dataset using Kaggle API in your Google Colab environment:
    ```bash
    !kaggle datasets download -d gpiosenka/100-bird-species
    ```

### Running the Project

1. Open the `bird_classification.ipynb` notebook in Google Colab.
2. Run each cell sequentially to preprocess the data, train the model, and evaluate its performance.

## Results

- Achieved 95.9% accuracy on the validation set.
- Achieved 97.32% accuracy on the test set, indicating strong generalization capabilities.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE.md) file for more details.

## Acknowledgments

- Kaggle for providing the [Bird Species 450](https://www.kaggle.com/datasets/gpiosenka/100-bird-species) dataset.
- Pytorch community for their valuable documentation and resources.
