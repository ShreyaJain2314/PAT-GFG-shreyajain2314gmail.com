# PAT-GFG-shreyajain2314gmail.com
Data Exploration :
The initial step involved a thorough exploration of the data to discern potential patterns, followed by the necessary adjustments to handle outliers.

Data Cleaning and Visualization Explanation:
Data Consistency: Invalid data (negative values or zero prices) were filtered out, and duplicates were removed, leaving 33,462 unique records.

Feature Engineering: Dropped the 'Booking_ID' column and grouped the 'lead_time' into categorical bins to capture ranges of lead times (Week, Month, etc.).

Visualization: Plotted a stacked bar chart showing the booking status (canceled or not) against these 'lead_time' groups, providing insights into cancellation trends. Afterwards, the distribution of values in the 'market_segment_type' column is printed.

Cancellation Analysis by Market Segment Explanation:
Data Preparation: For each market segment, the code calculates the percentage of bookings that were canceled.

Visualization: Using the calculated percentages, a bar chart is plotted for each market segment to visualize the cancellation rates.

Annotations: Each bar in the chart is annotated with the exact cancellation percentage value, providing a clear and informative representation of the data.

Machine Learning Workflow for Booking Cancellation Prediction:
Encoding Categorical Features: The categorical columns ('type_of_meal_plan', 'room_type_reserved', 'market_segment_type', 'booking_status') in the dataset are encoded using LabelEncoder to convert them into numeric values suitable for machine learning models.

Data Splitting: The dataset is split into predictors (features) and target (booking status). This data is then divided into a training set (70% of data) and a test set (30% of data).

Model Building and Evaluation: Initially, a Random Forest classifier is built and trained, followed by its evaluation on both training and test sets. Given signs of overfitting in this model, a second Random Forest classifier with additional hyperparameters (like max_depth, min_samples_split, etc.) is constructed to prevent overfitting. This revised model is trained, evaluated, and its feature importance is also displayed.
