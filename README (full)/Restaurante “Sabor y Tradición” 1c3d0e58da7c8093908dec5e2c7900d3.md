# <h1 align="center">Restaurante “Sabor y Tradición”</h1> (resumido)

# **Comprehensive data analysis for “Sabor y Tradición” restaurant**

## **Introduction**

This project was created for “Sabor y Tradición”, a restaurant aiming to improve its menu and gain a deeper understanding of its customers' preferences and habits. We developed a relational database that brings together menu details and order information, providing valuable insights to help with strategic decisions and enhance the overall customer experience. The solution is designed to work seamlessly in an SQL environment, combining the database framework with a set of analytical queries to tackle essential business questions.

---

## **Description**

The project is made up of the following key components:

- **Database**
  - **menu_items table:** Contains the menu options, including fields like ID, name, category, price, and, in some cases, a description or origin (e.g., Italian dishes).
  - **order_details table:** Tracks orders, with details such as dates, item quantities per order, total spending, and other relevant information.
- **Scripts**
  - It contains an SQL script that creates the restaurant's database, connects the tables, and establishes the required relationships between them.
  - Additionally, a data dictionary in CSV format is provided to document each field, offering clarity on the data structure and purpose.
- **Analytical Queries (RDB_O1, RDB_O2, RDB_O3)** Each script addresses key business questions and is organized into three objectives:
  1. Exploring the menu items table.
  2. Analyzing the orders table.
  3. Understanding customer behavior.

---

## **Objectives**

### **Objective 1: Explore the menu_items table**

The following tasks were carried out:

- **Viewing the menu_items table:** It provides a complete overview of all the dishes available on the menu.
- **Calculating the total number of items:** The COUNT() function is used to determine the total number of dishes offered.
- **Identifying the least and most expensive dishes:** The MIN() and MAX() functions are applied to the price field to establish the price range.
- **Filtering for Italian dishes:** A condition (e.g., WHERE category = 'Italian') is applied to count and analyze Italian cuisine options.
- **Analyzing prices for Italian dishes:** It identifies the least and most expensive Italian dishes.
- **Counting items by category and calculating average prices:** The GROUP BY clause is used to organize data and calculate average prices by category, offering a more segmented view of the menu.

### **Objective 2: Explore the orders table**

The tasks completed include:

- **Viewing the order_details table:** It provides a full display of the dataset of orders for overall understanding.
- **Determining the date range:** Aggregation functions and date formats are used to identify the time period covered in the table.
- **Counting orders and summing total items ordered:** The COUNT() function is applied to count orders, while SUM() calculates the total items, offering insights into transaction volumes.
- **Identifying orders with the highest number of items:** Data is sorted in descending order to highlight orders with the largest quantities.
- **Analyzing orders with more than 12 items:** It counts the number of orders exceeding this threshold, uncovering purchasing patterns.

### **Objective 3: Analyze customer behavior**

This objective focuses on the integration and combined analysis of both tables:

- **Merging menu_items and order_details tables:** The JOIN command is used to combine data for a comprehensive view of the relationship between the menu and orders.
- **Identifying the least and most ordered items and their categories:** Grouped counts are conducted to reveal customer preferences.
- **Determining the top 5 highest-spending orders:** Aggregation and sorting functions pinpoint the orders with the highest total value.
- **Details and insights on high-spending orders:** The highest-spending order and the top 5 costly orders are analyzed to understand consumption patterns, item combinations, and potential opportunities for promotions or menu adjustments.

---

## **Methodology and functions**

The project was built on a solid SQL-driven approach, leveraging query and aggregation techniques, including:

- **Aggregate functions:** COUNT(), SUM(), MIN(), MAX(), and AVG() were essential for calculating totals, averages, and identifying data extremes.
- **Filter and conditional operators:** WHERE was used to select specific subsets of data (e.g., identifying Italian dishes or filtering orders by item quantity).
- **Grouping and sorting:** The GROUP BY clause was used to organize information by category or date, while ORDER BY helped pinpoint key records, such as the highest-spending orders.
- **Table joins (JOINs):** Different JOIN types were applied to combine data from the menu_items and order_details tables. This allowed for a comprehensive customer behavior analysis based on the relationships defined in the database.

---

## Processes

### RDB_O1

**Objective 1**

The RDB_O1 script is divided into several sections, each addressing specific business questions. Here’s a breakdown of each part:

1. **Full view of the menu_items table**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.31.31 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.31.31_PM.png)
   - **Explanation:**
     - This query displays all records and fields in the menu_items table.
2. **Total number of items on the menu**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.33.27 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.33.27_PM.png)
   - **Explanation:**
     - The COUNT(\*) function is used to calculate the total number of records in the table.
     - This value serves as a benchmark for understanding the size of the restaurant's menu and can be compared in future analyses with filtered subsets (e.g., Italian dishes).
3. **Determining the least and most expensive items**
   - **Queries:**
     - _For the least expensive item:_
       ![Screenshot 2025-03-27 at 1.34.07 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.34.07_PM.png)
     - _For the most expensive item:_
       ![Screenshot 2025-03-27 at 1.34.35 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.34.35_PM.png)
   - **Explanation:**
     - Both queries sort the table by the price field, one in ascending order to identify the least expensive dish (e.g., Edamame) and the other in descending order to find the most expensive dish (e.g., Shrimp Scampi).
     - Adding a LIMIT 1 clause can restrict results to the single record that meets the condition.
4. **Counting and analyzing Italian dishes**
   - **Query for counting Italian dishes:**
     ![Screenshot 2025-03-27 at 1.34.56 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.34.56_PM.png)
   - **Explanation:**
     - The query calculates the total number of Italian dishes on the menu, highlighting their representation within the overall offerings.
     - It applies the WHERE clause to filter for dishes categorized as 'Italian.’
     - The COUNT(\*) function is then used to quantify these dishes.
   - **Queries for determining the least and most expensive Italian dishes:**
     - _Least expensive Italian dish:_
       ![Screenshot 2025-03-27 at 1.37.02 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.37.02_PM.png)
     - _Most expensive Italian dish:_
       ![Screenshot 2025-03-27 at 1.37.17 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.37.17_PM.png)
   - **Explanation:**
     - These queries combine the WHERE category = 'Italian' filter with sorting by price.
     - They identify the price extremes within the Italian dish subset.
     - _Least expensive Italian dish:_ the most affordable option (e.g., spaghetti), which appeals to budget-conscious customers.
     - *Most expensive Italian dish:* premium offerings like Shrimp Scampi.
5. **Counting items by category**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.38.31 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.38.31_PM.png)
   - **Explanation:**
     - It creates a list showing the number of dishes available in each category (e.g., Italian, American, Vegetarian, etc.).
     - GROUP BY organizes records by category.
     - COUNT() counts the items in each category.
6. **Calculating average price by category**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.38.50 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.38.50_PM.png)
   - **Explanation:**
     - It generates a list of categories with their average price, enabling category comparisons and assessment of whether pricing strategies align with perceived value.
     - The AVG(price) function calculates the average item price per category.
     - GROUP BY category segments the calculation.

**Summary of RDB_O1 Results**

- Reviewed the complete content of the menu_items table, confirming its structure and data range.
- Determined the total number of dishes using a count query.
- Identified the least and most expensive dishes, providing valuable insights for pricing strategies.
- The category count and average price calculations offered a detailed view of the menu, revealing potential areas for improvement or expansion.

**Objective 2**

The RDB_O2 script focuses on obtaining a comprehensive view of the restaurant's order activity:

1. **Full view of the order_details table**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.42.27 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.42.27_PM.png)
   - **Explanation:**
     - It displays all records and fields in the order_details table to ensure the structure and information are correctly stored.
2. **Determining the date range**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.44.19 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.44.19_PM.png)
   - **Explanation:**
     - It identifies the time period covered by the recorded orders.
     - MIN() and MAX() functions are used to find the earliest and latest dates, respectively.
     - This range helps in understanding the analysis period and spotting trends over time.
3. **Total number of orders**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.45.01 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.45.01_PM.png)
   - **Explanation:**
     - It counts the total number of orders placed during the recorded period.
     - COUNT(\*) function iterates through all records in the order_details table to provide a total count.
     - It returns a single numeric value reflecting the total order volume, offering insights into the restaurant’s activity.
4. **Total number of items ordered**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.45.24 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.45.24_PM.png)
   - **Explanation:**
     - It calculates the total number of items sold during the analysis period.
     - It provides a numeric value representing total items sold, a key metric for inventory and marketing strategies.
5. **Identifying orders with the highest item count**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.45.47 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.45.47_PM.png)
   - **Explanation:**
     - It highlights orders with the largest number of items, potentially indicating high-volume purchases or special requests.
     - Results can be used to analyze behavior patterns of customers placing large orders, uncover trends, and design targeted promotions.
     - Query sorts records in descending order by the item count.
6. **Counting orders with more than 12 items**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.46.03 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.46.03_PM.png)
   - **Explanation:**
     - It determines how many orders exceeded 12 items, reflecting specific purchase behaviors or group order needs.
     - Useful for identifying trends and deciding whether to implement special strategies for large orders, such as discounts or promotions.

---

---

### RDB_O2

**Summary of RDB_O2 Results**

The main findings are:

- The initial query provides a full view of all order details, ensuring that the database is properly structured.
- It identifies the date range covered by the records, which is crucial for performing time-based analyses and spotting seasonal patterns.
- It calculates the total number of orders and adds up the total items sold, offering key metrics for assessing commercial activity and performance.
- Identifying orders with the highest number of items and counting those that exceed 12 items helps pinpoint special customers or situations that could benefit from targeted business strategies.

**Objective 3**

Each section is detailed below:

1. **Combining the menu_items and order_details tables**
   - **Explanation:**
     - The first step involves viewing each table individually and then combining them to gain a comprehensive perspective.
     - It provides a full display of all records in each table to review their structure and content.
     - This step ensures that data is properly loaded and highlights available fields, such as identifiers, names, categories, and prices from menu_items, as well as order details from order_details.
     - A LEFT JOIN is used to merge the order_details table with the menu_items table, using the item_id field in order_details and the menu_item_id field in menu_items as the key.
     - The LEFT JOIN ensures that all orders are preserved, even if some don’t have a matching menu item (for example, due to errors or pending validation).
2. **Identifying the least and most ordered items and their categories**
   - **Query to view how many times each item was ordered (descending order):**
     ![Screenshot 2025-03-27 at 1.54.08 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.54.08_PM.png)
   - **Query for the least ordered item (ascending order):**
     ![Screenshot 2025-03-27 at 1.54.29 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.54.29_PM.png)
   - **Query for the most ordered item (descending order):**
     ![Screenshot 2025-03-27 at 1.54.58 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.54.58_PM.png)
   - **Explanation:**
     - The query calculates the number of records in order_details associated with each item_name using the COUNT(order_details_id) function.
     - Data is grouped by item_name to consolidate the total purchases for each product.
     - Sorting in descending order (ORDER BY num_purchases DESC) makes it easy to identify the most requested items.
     - Adding the category field to the GROUP BY clause provides extra insights into the category of each item.
     - Sorting in ascending order identifies the least ordered item, while descending order highlights the most popular one.
     - For example:
       - It identifies the least ordered item (e.g., chicken tacos) and its category (e.g., Mexican), helping assess whether it’s a niche product or simply unpopular.
       - It also highlights the most ordered item (e.g., hamburger) and its category (e.g., American), helping emphasize menu successes and potential areas for investment or promotion.
3. **Top 5 highest-spending orders**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.55.20 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.55.20_PM.png)
   - **Explanation:**
     - The query determines the total amount spent on each order by summing the item prices with the SUM(price) function, grouping the results by order_id.
     - The results are sorted in descending order and limited to the top 5 (LIMIT 5).
     - This analysis is essential for identifying premium spending patterns and evaluating the success of strategies targeting high-value orders.
4. **Details of the highest-spending order**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.55.38 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.55.38_PM.png)
   - **Explanation:**
     - The query narrows down the combined table to focus specifically on the highest-spending order (order_id = 440).
     - The data is grouped by category, and the number of items in each category is counted (COUNT(item_id)).
     - The insights include:
       - If the order focuses heavily on one category, it could indicate a strong preference.
       - A mix of categories might suggest opportunities for upselling or highlight popular menu combinations in high-value orders.
5. **Details of the top 5 highest-spending orders**
   - **Query:**
     ![Screenshot 2025-03-27 at 1.55.56 PM.png](Restaurante%20%E2%80%9CSabor%20y%20Tradicio%CC%81n%E2%80%9D%201c3d0e58da7c8093908dec5e2c7900d3/Screenshot_2025-03-27_at_1.55.56_PM.png)
   - **Explanation:**
     - The query focuses on filtering the previously identified top 5 highest-spending orders (e.g., 440, 2075, 1957, 330, 2675) to analyze their details more specifically.
     - Grouping by order_id and category reveals the number of items per category for each high-value order.
     - The insights derived include:
       - Identifying common patterns among high-spending orders, such as dominance of a specific category.
       - Evaluating whether the category combinations in high-value orders suggest potential for special menus or promotions that could be replicated in future strategies.
       - Spotting opportunities to improve offerings, such as creating bundled dishes to increase the average ticket value.

---

### RDB_O3

**Summary of RDB_O3**

Running the RDB_O3 script revealed several insights into customer behavior and how menu offerings align with orders placed. Key findings include:

- The analysis merges the menu_items and order_details tables, providing a comprehensive view that links each order to its corresponding menu details.
- The least and most ordered items are identified along with their categories, offering insights into which products are successful and which may benefit from adjustments or promotional efforts.
- Spending per order is analyzed and further broken down by category in the highest-spending orders, revealing trends in premium purchases. These insights can support upselling strategies and enhance the customer experience for larger orders.
- The composition of the highest-spending orders is evaluated, creating opportunities to design targeted promotions or modify the menu to encourage combinations that maximize ticket values and increase revenue.

**General project results**

- **Menu exploration:**
  - The full range of dishes was reviewed, confirming the menu’s variety.
  - The total number of available items was identified.
  - Price ranges were analyzed, clearly distinguishing the least and most expensive items.
  - The count of Italian dishes and their price range was calculated, offering insights into the category’s competitiveness.
  - Segmenting by category highlighted the number of dishes and average price in each group, enabling internal comparisons for potential menu adjustments.
- **Order analysis:**
  - The date range for orders was established, providing a foundation for analyzing sales trends and seasonal variations.
  - Quantitative data on the total number of orders and items sold during the period was captured.
  - High-volume orders, including those exceeding 12 items, were identified, presenting opportunities for promotions or discounts targeting bulk orders.
- **Customer behavior:**
  - By integrating the tables, the analysis was able to pinpoint the most and least popular items, providing essential insights to help refine the menu and improve overall offerings.
  - The economic analysis highlighted the top 5 highest-revenue orders, allowing for detailed examination of dish combinations and customer preferences.
  - A closer look at the highest-spending order and the top 5 orders revealed consumption patterns, such as preferences for certain dishes or combinations. These findings are critical for developing marketing strategies and refining the menu.

---

### **Conclusions and recommendations**

This project has provided "Sabor y Tradición" with a detailed understanding of its operations, focusing on both menu performance and customer purchasing patterns. Key takeaways include:

- The analysis highlighted the need to adjust pricing and reevaluate certain categories to stay competitive and maximize profits.
- Identifying orders with high item counts and significant spending presents an opportunity to create targeted promotions or discounts that can drive sales and enhance customer loyalty.
- Incorporating analyses of seasonality (e.g., monthly or seasonal trends) and geographic segmentation (if available) is recommended to further tailor marketing strategies and boost effectiveness.

---

```html
<p align="center">
  <big><strong>✨¡Gracias por visitar este repositorio!✨</strong></big>
</p>
```
