# housing-price-prediction

Using multiple machine learning models to predict the price of houses based on listing data (e.g., square footage, num stories, num bedrooms). See [housing.ipynb](/housing.ipynb) for full implementation.

![Error in housing price predictions](/images/error-comparison.png)

Notes:
- The reported MSE values (in white) are on the log-transformed SalePrice.
- I also include the Mean Absolute Error (MAE, in black) on the original SalePrice. This allows for an interpretible result in a dollar amount.

## Conclusions
- SVM performs best with XGBoost coming in a close second.
- Across the board, the prediction accuracy is reasonably good. Our best models predict with MAE accuracy closer than 10% of the average sale price.
- RF and XGBoost could have been improved by using a restricted GridSearchCV. I did not refine these models after the RandomSearchCV since they are computationally costly to train.
- The MLP's performance is slightly worse than most other methods (except KNN).
- I could have tried deeper/wider (>9 layers/neurons) networks, but the performance is reasonable despite the shallowness/narrowness of the model.
