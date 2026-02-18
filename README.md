#  User Engagement & Purchase Funnel Analysis

This project analyzes user engagement, purchase funnel performance, and customer purchasing behavior using three datasets: Events, Orders, and Customers.

The objective was to clean the data, perform structured analysis, and generate meaningful business insights supported by visualizations.

---

##  Dataset Description

### 1️ Events Data
- `user_id`
- `event_date`
- `event_name`

### 2️ Orders Data
- `order_id`
- `customer_id`
- `order_date`
- `order_status`
- `net_sales`
- `disc`

### 3️ Customers Data
- `customer_id`
- `registered_date`
- `city`
- `acquistion_channel`

---

##  Question 1: Data Cleaning & Preparation

Before performing analysis, the datasets were cleaned to ensure consistency and accuracy.

### Cleaning Steps:

- Removed fully empty rows  
- Removed rows with missing primary keys (`user_id`, `customer_id`, `order_id`)  
- Converted date columns to proper datetime format  
- Removed invalid or null date values  
- Filtered only valid orders (`order_status = 'valid'`)  
- Removed null or negative revenue values  
- Filled missing categorical values where necessary  
- Removed duplicate records  
- Standardized ID columns for accurate joins  

### Assumptions:

- `user_id` corresponds to `customer_id`  
- Only valid orders represent successful revenue transactions  
- Missing acquisition channel values treated as "organic"  
- `net_sales` represents final transaction value  

---

##  Question 2: User Engagement → Purchase Funnel

### Funnel Metrics:

- **Users with Events:** 147,336  
- **Users with Valid Orders:** 28,463  
- **Conversion Rate:** 19.32%

### Analysis Performed:

- Counted unique users who triggered any event  
- Counted unique users who placed at least one valid order  
- Calculated conversion rate  
- Created a daily trend visualization comparing:
  - Active users  
  - Ordering customers  

### Key Insight:

Although user engagement is strong, only a portion of users convert into paying customers. This indicates an opportunity to optimize the conversion funnel and improve purchase completion rates.

---

##  Question 3: Customer Behavior Insight

To understand purchasing behavior:

- Joined customers and orders datasets using `customer_id`
- Aggregated total revenue by acquisition channel
- Identified the highest revenue-generating channel
- Visualized results using a bar chart

### Key Insight:

The leading acquisition channel generates the highest total revenue, indicating it is currently the strongest revenue driver. Further evaluation of customer acquisition cost (CAC) would help assess long-term profitability.

---

##  Visualizations Included

-  Daily Active Users vs Ordering Customers  
-  Revenue by Acquisition Channel  
-  Visualization Report (PDF)

---

##  Tools & Technologies

- Python  
- Pandas  
- Matplotlib  
- Jupyter Notebook  

---

##  Overall Conclusion

The platform demonstrates strong user engagement but a moderate conversion rate (~19%). By improving the conversion journey and focusing on high-performing acquisition channels, the business can increase revenue and improve marketing efficiency.

