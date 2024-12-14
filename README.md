# upliance.ai-assignment
### Updated README: Combining User, Session, and Order Data with Graph Analysis

#### **1. Project Overview**
This project integrates three datasets (`users_data`, `sessions_data`, and `orders_data`) into a single comprehensive dataset for deeper analysis. Additionally, it provides insights through visualizations that highlight user behavior, revenue trends, and meal preferences.

#### **2. Required Files**
Ensure you have the following files in the same directory:
1. **users_data.csv**: Contains user details.
   - Columns: `User ID`, `User Name`, `Age`, `Location`, `Registration Date`, `Phone`, `Email`, `Favorite Meal`, `Total Orders`
2. **sessions_data.csv**: Contains session-related data.
   - Columns: `User ID`, `Session ID`, `Dish Name`, `Meal Type`, `Session Start`, `Session End`, `Duration (mins)`, `Session Rating`
3. **orders_data.csv**: Contains order-related details.
   - Columns: `Session ID`, `Order ID`, `Order Date`, `Meal Type`, `Dish Name`, `Order Status`, `Amount (USD)`, `Time of Day`, `Rating`

#### **3. Process Description**
The merging process aligns data from the three datasets:
1. **Step 1**: Merge `sessions_data` and `orders_data` on the `Session ID` column using an inner join. This ensures that only matching session and order records are combined.
2. **Step 2**: Merge the result with `users_data` on the `User ID` column using an inner join. This adds user information to the combined dataset.

#### **4. Graphical Analysis**
Key visualizations provide insights into the combined data:
1. **User Behavior**: 
   - **Bar Chart**: Total orders by age group (`<26`, `26-35`, `36-45`, `>45`).
   - **Scatter Plot**: Relationship between session duration and session ratings.
2. **Revenue Trends**:
   - **Bar Chart**: Total revenue by location.
   - **Pie Chart**: Revenue contribution by meal type (Breakfast, Lunch, Dinner).
3. **Meal Preferences**:
   - **Horizontal Bar Chart**: Most preferred meals based on total orders.
   - **Line Chart**: Variation in orders across times of the day (Morning, Afternoon, Evening).
4. **Top Dishes and Order Status**:
   - **Bar Chart**: Top 5 most ordered dishes.
   - **Pie Chart**: Distribution of order statuses (Completed, Pending, Cancelled).

These visualizations are generated using Python libraries like `Matplotlib` and `Seaborn`.

#### **5. Output**
1. **Combined Data**: The resulting dataset, `final_combined_data.csv`, contains:
   - **User Data**: `User ID`, `User Name`, `Age`, `Location`, `Registration Date`, `Phone`, `Email`, `Favorite Meal`, `Total Orders`
   - **Session Data**: `Session ID`, `Dish Name` (from sessions), `Meal Type` (from sessions), `Session Start`, `Session End`, `Duration (mins)`, `Session Rating`
   - **Order Data**: `Order ID`, `Order Date`, `Meal Type` (from orders), `Dish Name` (from orders), `Order Status`, `Amount (USD)`, `Time of Day`, `Rating`

2. **Visual Insights**: Generated as PNG files or displayed interactively in Jupyter Notebook.



