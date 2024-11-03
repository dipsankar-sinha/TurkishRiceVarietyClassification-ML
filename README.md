# Turkish Rice Variety Classification

## Project Overview
This project focuses on classifying two rice varieties, Cammeo and Osmancik, based on morphological features extracted from images of rice grains. The dataset consists of 3810 images, and our objective is to build a reliable classification model using machine learning techniques.

## Dataset Information
- **Dataset Name**: Rice Dataset (Cammeo and Osmancik)
- **Source**: 
  - Ilkay Cinar, Graduate School of Natural and Applied Sciences, Selcuk University, Konya, Turkey. (ilkay_cinar@hotmail.com)
  - Murat Koklu, Faculty of Technology, Selcuk University, Konya, Turkey. (mkoklu@selcuk.edu.tr)
- **Link to Dataset**: [Rice Dataset](https://www.muratkoklu.com/datasets/)
- **Link to Used Dataset Available on UCI Repository**: [Open_in_UCI_Repository](https://archive.ics.uci.edu/dataset/545/rice+cammeo+and+osmancik)
- **Link to Colab Notebook**: [Open_in_Colab](https://colab.research.google.com/drive/1sxRF6JruDAswLK4i4JQURIIa87Meon-p?usp=sharing)

### Features
The dataset includes the following features:
1. **Area**: Number of pixels within the boundaries of the rice grain (px).
2. **Perimeter**: Circumference calculated by pixel distances around the boundaries (px).
3. **Major Axis Length**: Longest line that can be drawn on the rice grain.
4. **Minor Axis Length**: Shortest line that can be drawn on the rice grain.
5. **Eccentricity**: Measure of how round the ellipse that matches the rice grain is.
6. **Convex Area**: Pixel count of the smallest convex shell of the rice grain region.
7. **Extent**: Ratio of the rice grain region to the bounding box pixels.
8. **Class**: Indicates the rice variety (Cammeo or Osmancik).

## Data Preprocessing
### Normalization
- Z-score normalization was applied to the features to standardize the data.

### Outlier Detection and Removal
- Extreme outliers were identified and removed using the Z-score method with a threshold of 3.

### Data Splitting
- The dataset was split into training and testing sets:
  - **Train Data Shape**: (3020, 8)
  - **Test Data Shape**: (756, 8)

### Class Distribution
After outlier removal, the class distribution is as follows:
- **Osmancik**: 2154 samples
- **Cammeo**: 1622 samples

## Model
- **Algorithm Used**: Logistic Regression
- The model was trained on the preprocessed training data.

## Model Performance
### Classification Report
| Class    | Precision | Recall | F1-Score | Support |
|----------|-----------|--------|----------|---------|
| Cammeo   | 0.93      | 0.89   | 0.91     | 341     |
| Osmancik | 0.91      | 0.95   | 0.93     | 415     |

- **Overall Accuracy**: 0.92
- **Macro Average**: 
  - Precision: 0.92 
  - Recall: 0.92 
  - F1-Score: 0.92
- **Weighted Average**: 
  - Precision: 0.92 
  - Recall: 0.92 
  - F1-Score: 0.92

## Conclusion
The Logistic Regression model achieved a classification accuracy of 92%, indicating strong performance in distinguishing between the Cammeo and Osmancik rice varieties. Future work could involve exploring additional machine learning algorithms and techniques to enhance classification accuracy.

## Relevant Papers
Cinar, I. & Koklu, M. (2019). Classification of Rice Varieties Using Artificial Intelligence Methods. *International Journal of Intelligent Systems and Applications in Engineering*, 7(3), 188-194. [Link to paper](https://doi.org/10.18201/ijisae.2019355381).

## Acknowledgments
I extend my gratitude to the contributors of the dataset and the researchers involved in the study.
