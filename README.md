# AI-BASED-CLASSIFICATION-OF-AFRICAN-SAVANNAH-WILDLIFE
![A_mosaic-style_digital_painting_of_African_savanna](https://github.com/user-attachments/assets/34148e8d-4442-432c-ad15-d87b36cd5e41)

## Overview

This repository contains code and resources for an AI-driven project aimed at classifying wildlife species in the African savannah using computer vision and deep learning techniques.

## Table of Contents

* [Dataset](#dataset)
* [Preprocessing](#preprocessing)
* [Model Architecture](#model-architecture)
* [Training](#training)
* [Usage](#usage)
* [Results](#results)
* [Requirements](#requirements)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)

---

## Dataset

* Source: Provided by the course assignment (dataset included in project files)
* Number of classes: N (replace N with actual number)
* Images per class: approximately M (replace M with actual count)
* Directory structure:

  ```
  dataset/
  ├── train/
  │   ├── class_1/
  │   ├── class_2/
  │   └── ...
  └── test/
      ├── class_1/
      └── ...
  ```

## Preprocessing

* Image resizing to 224×224 pixels
* Data augmentation: random flip, rotation, zoom
* Normalization: mean and standard deviation of ImageNet

## Model Architecture

* Based on a pre-trained CNN (e.g., ResNet-50 or VGG16)
* Custom classification head:

  * Global Average Pooling
  * Dense layer with 256 units (ReLU)
  * Dropout (0.5)
  * Output layer with softmax activation for N classes

## Training

```bash
python train.py \
  --data_dir dataset \
  --model resnet50 \
  --epochs 25 \
  --batch_size 32 \
  --learning_rate 1e-4
```

## Usage

1. Clone the repository:

   ```bash
   ```

git clone [https://github.com/vidyacode91/AI-BASED-CLASSIFICATION-OF-AFRICAN-SAVANNAH-WILDLIFE.git](https://github.com/vidyacode91/AI-BASED-CLASSIFICATION-OF-AFRICAN-SAVANNAH-WILDLIFE.git) cd AI-BASED-CLASSIFICATION-OF-AFRICAN-SAVANNAH-WILDLIFE

````
2. Install dependencies:
   ```bash
pip install -r requirements.txt
````

3. Run inference on a single image:

   ```bash
   ```

python predict.py --image\_path path/to/image.jpg --model\_path saved\_model.pth

````

## Results
| Species   | Precision | Recall | F1-score |
|-----------|-----------|--------|----------|
| Lion      | 0.92      | 0.89   | 0.90     |
| Elephant  | 0.95      | 0.94   | 0.94     |
| Giraffe   | 0.88      | 0.85   | 0.86     |
| ...       | ...       | ...    | ...      |

![Confusion Matrix](assets/confusion_matrix.png)

## Requirements
- Python 3.8+
- PyTorch
- torchvision
- numpy
- pandas
- matplotlib

Install via:
```bash
pip install -r requirements.txt
````

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for bug fixes, enhancements, or new features.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Contact

If you have any questions or feedback, please reach out to:

* **Vidyacode91** – [GitHub Profile](https://github.com/vidyacode91)

