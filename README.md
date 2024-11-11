# Diabetes Detection using Multilayer Perceptron (MLP)

This project builds an MLP model using Keras and TensorFlow to predict the onset of diabetes within five years based on patient data.

## Data

The project uses the "diabetes.csv" dataset. This dataset contains features such as:

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

The target variable is 'Outcome', which indicates whether the patient developed diabetes (1) or not (0).

## Preprocessing

The following preprocessing steps were applied to the data:

1. **Handling Missing Values:** Zeros in features like 'Glucose', 'BloodPressure', 'SkinThickness', 'Insulin', and 'BMI' were replaced with NaN and then imputed with the mean value of the respective feature.
2. **Scaling:** All features were scaled using `preprocessing.scale` to bring them to a similar range.

## Model Building

A Sequential model was built using Keras with the following architecture:

- **Input Layer:**  With input dimensions matching the number of features.
- **Hidden Layers:** Two Dense layers with ReLU activation (32 and 16 neurons respectively).
- **Output Layer:** A Dense layer with a sigmoid activation function to predict the probability of diabetes.

## Training and Evaluation

The model was trained using the Adam optimizer and binary cross-entropy loss function. The dataset was split into training, validation, and testing sets. Training was performed for 201 epochs, and the model's performance was evaluated on the testing set using accuracy as the metric.

## Results

The model achieved a training accuracy of approximately 92% and a testing accuracy of approximately 77%. However, signs of overfitting were observed, indicating a need for further optimization or regularization techniques.

## Conclusion

This project demonstrates the use of an MLP for diabetes prediction. While the model shows promising results, addressing overfitting is crucial for improved generalization and real-world performance.
