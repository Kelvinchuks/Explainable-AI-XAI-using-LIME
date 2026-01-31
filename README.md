# Explainable-AI-XAI-using-LIME
**Objective**: To move beyond simple accuracy and understand why a Deep Learning model makes specific predictions on a banking dataset.
### The Problem: The Accuracy Paradox
* The Model: A Neural Network was trained on a banking dataset and achieved ~89% accuracy.
* The Issue: High accuracy was misleading due to an imbalanced dataset (mostly "No" answers). The model acted as a "Black Box," providing predictions without explanations, which is unacceptable in regulated industries like banking.
### The Solution: LIME (Local Interpretable Model-agnostic Explanations)
* Model-Agnostic: LIME treats the model as a black box and only requires inputs and outputs to function.
* Local Fidelity: It trains a simple, interpretable linear model locally around a specific data point to approximate the complex model's behaviour.
### Project Highlights & Findings
* Built a Black Box: Created a Neural Network for banking predictions.
* Implemented LIME from Scratch: Used LIME to explain individual rejection decisions.
* Discovered Data Leakage: The audit revealed that the model relied heavily on "Call Duration." This is a form of data leakage, as duration is only known after a call is completed, making it a "flaw" in a high-accuracy model.
* Validation: Findings were validated using a transparent Decision Tree (Glass Box), which confirmed "duration" as the most critical feature.
### Conclusion
This project demonstrates that LIME is a powerful tool not only for explaining decisions to clients but also for detecting hidden flaws and data leakage in high-performing models.
