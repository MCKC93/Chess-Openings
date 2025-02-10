# Chess Openings Predict the best defense given White's opening type

## 📌 Project Overview  
This project is a **data science exercise** focused on analyzing the best defensive moves for Black based on White's openings in chess. Using the **High-Elo Games Chess Opening Dataset** from Kaggle, I applied **machine learning techniques** to predict Black's optimal responses. My initial approach leverages a **Random Forest model**, chosen for its interpretability and efficiency.  

**Note:** This is a learning project, and I welcome any feedback, comments, or suggestions for improvement!  

## Dataset  
- **Name:** [High-Elo Games Chess Opening Dataset](https://www.kaggle.com/datasets)  
- **Description:** A dataset containing chess games played by high-rated players, focusing on the first moves of both White and Black.  
- **Key Features:**  
  - `move1w`, `move2w`, `move3w`, `move4w`: White’s first four moves  
  - `move1b`, `move2b`, `move3b`, `move4b`: Black’s responses  
  - `opening_name`: Name of the chess opening  

##  Machine Learning Approach  
### Why Random Forest?  
I chose **Random Forest** because:  
✅ It is easy to interpret and efficient to train.  
✅ It handles categorical data well (chess moves).  
✅ It reduces overfitting by aggregating multiple decision trees.  

### Model Training & Evaluation  
- The dataset was **preprocessed** and split into **training (80%) and test (20%)** sets.  
- A **Random Forest Classifier** was trained using `sklearn.ensemble.RandomForestClassifier`.  
- I evaluated the model using **precision scores** for each predicted move.  
- Results showed that **predictability decreases as moves progress**, highlighting the complexity of later moves.  

## Results  
| Move  | Precision Score |
|--------|----------------|
| Move 1b | 0.73 |
| Move 2b | 0.70 |
| Move 3b | 0.63 |
| Move 4b | 0.31 |

As expected, predictions for the **first Black move are more accurate**, while later moves become increasingly difficult to predict due to the growing complexity of the game.  

## Future Improvements  
🔹 **Explore sequence-based models (LSTM/GRU)** to capture dependencies between moves.  
🔹 **Optimize the Random Forest model** (hyperparameter tuning, class balancing).  
🔹 **Test alternative ML models** (Gradient Boosting, XGBoost).  
🔹 **Feature engineering**: Incorporate game metadata for better context.  

##  Author  
**MCKC93**  
 

## Contributing  
This project is open for contributions! Feel free to **fork** the repository, submit **pull requests**, or share your insights via **issues**.  

## 📜 License  
This project is licensed under the **MIT License** – feel free to use, modify, and share.  

---

**Any feedback or suggestions are highly appreciated!** Thanks for checking out this project! 
