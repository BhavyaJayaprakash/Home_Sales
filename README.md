## Home_Sales
Module 22 challenge
## Background

 In this challenge, you'll use your knowledge of SparkSQL to determine key metrics about home sales data. Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

 ## Instructions and Results
1. Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.
2. Import the necessary PySpark SQL functions for this assignment.
   
  ![image](https://github.com/user-attachments/assets/d2271d84-78fc-4a96-a4e3-749e65a1b6d9)

3. Read the home_sales_revised.csv from the provided AWS S3 bucket location into a PySpark DataFrame.

 ![Screenshot 2025-04-03 214335](https://github.com/user-attachments/assets/4cbe8edb-c496-4621-bc1a-324f15d5a60a)

4. Create a temporary table called home_sales.

 ![Screenshot 2025-04-03 214352](https://github.com/user-attachments/assets/5434ef97-db7a-4f86-a1de-b551ea19691c)

5. Answer the following questions using SparkSQL:
  What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

![Screenshot 2025-04-03 214417](https://github.com/user-attachments/assets/dcbb94ce-ef5b-491a-8ad0-b0db045c5546)


 6. What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

  
  ![Screenshot 2025-04-03 214451](https://github.com/user-attachments/assets/95f1b4ef-677c-4832-a207-75eb685f4ef5)

 7. What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
  
  ![Screenshot 2025-04-03 214518](https://github.com/user-attachments/assets/a2c28bb5-bbdf-4b88-a778-0ecfdca9cad9)

8. What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

![Screenshot 2025-04-03 214553](https://github.com/user-attachments/assets/a18da421-e395-41d2-bb9b-5fbbefed2926)
![Screenshot 2025-04-03 214600](https://github.com/user-attachments/assets/be46e69d-91c7-466b-8017-71d77e40edb2)

8. Cache your temporary table home_sales.
10. Check if your temporary table is cached.

    ![Screenshot 2025-04-03 214627](https://github.com/user-attachments/assets/52acef02-1f0d-43f6-82ac-120087bcf426)

12. Using the cached data, run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

    ![Screenshot 2025-04-03 214712](https://github.com/user-attachments/assets/c40f3dda-d28e-40a8-a15f-8b6e4b51021e)
   ![Screenshot 2025-04-03 214719](https://github.com/user-attachments/assets/f4de3166-f7f8-4ead-a5f0-e7216b7577c6)

# Uncached Runtime --- 1.0180721282958984 seconds ---
# Cached Runtime --- 0.6322424411773682 seconds ---

14. Partition by the "date_built" field on the formatted parquet home sales data.
16. Create a temporary table for the parquet data.
17. 
![Screenshot 2025-04-03 214850](https://github.com/user-attachments/assets/4a5af0c4-573a-4535-9fa9-3783184f3ca8)

   
19. Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
Uncache the home_sales temporary table.

![Screenshot 2025-04-03 214935](https://github.com/user-attachments/assets/f97fbba8-9c50-434e-b215-14caaba69fc6)

![Screenshot 2025-04-03 214943](https://github.com/user-attachments/assets/5a7f50e3-b92a-44ef-b109-0f60d33272b5)

21. Verify that the home_sales temporary table is uncached using PySpark.

 # Uncached Runtime --- 1.0180721282958984 seconds ---
# Cached Runtime --- 0.9337108135223389  seconds ---

23. Download your Home_Sales.ipynb file and upload it into your "Home_Sales" GitHub repository.
