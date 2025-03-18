
# Team 4: El Quatro Bakery Cafe (MIST 4610 GroupProject1)

## Team Name
Sp25_21479_Group4

## Team Members 
   1. Lauryn Stallworth
   2. Abby Poore
   3. Claire Warren 
   4. Liam Aiken
   5. Nick Weir

## Scenario Description

As five innovative coffee lovers, we were tasked with developing a database for the operations of our new business El Quatro Bakery & Cafe. We chose to start this business because we have all experience working as former baristas or restaurant employees. Given our background, we wanted to take the organization of El Quatro Bakery & Cafe to the next level through the use of a structured database. Utilizing this database will allow us to track different aspects of our daily operations such as our customers, employees, inventory, and delivery. These key parts of our business have interconnected relationships which are visible within the database. The central focus of our data model is our orders where each order is linked to a customer, an employee handling the transaction, payment details, and the specific menu items purchased. This system will help us optimize order processing, payment tracking, customer connections, employee performance, and decision making based on our analyzed data.

## Data Model

Our model represents the structure of a bakery’s operations that we have named El Quatro. 

The Customers entity holds details about customers, including their names, email, address, etc. Customers can enroll in a LoyaltyProgram, which will help keep track of their loyalty points and enrollment date. Additionally, customers make Payments for their orders, this is a one to many relationship between Payments and Customers because one Customer can make multiple Payments but each Payment only has one Customer. 
Customers place Orders at our bakery establishing a one to many relationship because each Customer can place multiple orders, however each order only has one customer. Each order is associated with a specific Employee who handles the transaction. Each of our Employees can handle many Orders. Since an Order consists of multiple items, we made an OrderItems table that links orders with individual MenuItems, tracking quantities and prices for each Item. The OrderItems acts as an associative table and establishes a many to many relationship between the two entities. 

The MenuItems entity lists all available bakery items, including their names, prices, type, and descriptions. Each menu item requires various Ingredients, which are stored in the Inventory table. Inventory and Ingredients has a one to one relationship because each inventory record will correspond to one ingredient, and each ingredient has one inventory entry. Inventory will  track ingredient stock levels, types, and suppliers. A many-to-many relationship exists between MenuItems and Ingredients. This is represented by our creation of the Recipe_has_ingredients table, which stores ingredients' primary key (ingredientID) and menuItems primary key (itemID) as foreign keys. This table further specifies ingredient quantities and preparation notes for each menu item.
The Suppliers table will keep records of external vendors that provide ingredients for our bakery. Each supplier is linked to specific inventory items, allowing for tracking of supply sources. This establishes a one to many relationship because the supplier supplies many inventory items, but each inventory item only has one supplier. 
The bakery also manages Employees, whose details include roles, salaries, emails, etc… are stored in the Employees table. Employee schedules are managed through the EmployeeSchedule table and this is a one to many relationship because an Employee can have many shifts over time, but each individual shift only has one employee.

We have the option of having our food and drinks delivered. The Delivery table will track each of these deliveries, including tracking pickup and delivery times, statuses, and associated orders. Deliveries are assigned to DeliveryDrivers and this relationship is a one to many relationship as each delivery driver can have multiple deliveries, but each delivery only has one delivery driver. Delivery and Order will have a one to one relationship because each delivery is assigned to one order and each order only has one corresponding delivery. 
This structured model allows our bakery to efficiently manage its customers, orders, employees, inventory, and deliveries while maintaining strong supplier relationships and a loyalty program.

<img width="1136" alt="424117249-c7df385e-5830-43a5-abe0-104ec4ddc92f (1)" src="https://github.com/user-attachments/assets/c13f9462-6ef3-4cca-b723-961765fc5c85" />


## Data Dictionary

<img width="764" alt="424127756-24258f52-7b1f-487e-aec7-717c2234829d" src="https://github.com/user-attachments/assets/51e532d0-d9f3-4149-8e14-eb4fc70d8427" />

<img width="782" alt="424127550-3c318f9e-8809-4fc9-ab8e-b9df1839dc84" src="https://github.com/user-attachments/assets/6482328f-ea76-469f-a421-bc4d372849a0" />

<img width="752" alt="424127918-163a6827-17a9-4bc5-a4cb-ec8827a10818" src="https://github.com/user-attachments/assets/49920df1-2c0a-4e43-9657-2f337a511ecb" />

<img width="778" alt="424128441-4859ae00-352d-475f-b882-92795da51edf" src="https://github.com/user-attachments/assets/9d2004d9-0822-45e5-af34-565c5d1fbf73" />

<img width="767" alt="424128955-eff62228-ff24-411b-818e-5702ed4a797b" src="https://github.com/user-attachments/assets/4873d3ad-5549-414f-afbb-78c6cf3fe521" />

<img width="765" alt="424129184-97c9b70a-122a-4495-b335-e5d470f7dd94" src="https://github.com/user-attachments/assets/ba097d19-7718-4276-9b96-fdb989dfb533" />

<img width="716" alt="424129766-f21cb759-a739-4daf-a9ea-aceb712af729" src="https://github.com/user-attachments/assets/3b6a519d-3fca-463f-a132-da2580414a2e" />

<img width="775" alt="424130086-312795ba-dde5-45b6-bd49-7fbda606367d" src="https://github.com/user-attachments/assets/52efd3c1-0081-4421-8574-519bc468f001" />

<img width="755" alt="424130249-ded6d70b-1157-4436-8f34-29cfcb83d7ec" src="https://github.com/user-attachments/assets/cc9b3b0d-348e-4c18-87a2-5c6fe082a841" />

<img width="774" alt="424130556-c7bf422a-c3fa-4965-95c0-0f3e6e0cd608" src="https://github.com/user-attachments/assets/9bfccdb8-c0aa-4c4d-9310-2f19709f93c5" />

<img width="767" alt="424130742-c8ffdc83-00bd-4915-9f21-632aeb59403d" src="https://github.com/user-attachments/assets/72b26f1b-1e61-4b92-ab4d-00e20697d1c2" />

<img width="718" alt="424131381-f738fd1c-fc64-4a9a-a371-5b14115c9388" src="https://github.com/user-attachments/assets/23438732-46cd-4d6e-8d10-92567f2d4043" />

<img width="716" alt="424132152-22e680c2-b3fb-4f1a-b633-83da78d63516" src="https://github.com/user-attachments/assets/15a0665b-7829-4438-81f8-b45a8f3c6ab3" />

<img width="782" alt="424133319-cd23f45b-a424-4f70-ab91-2540f0cd6990" src="https://github.com/user-attachments/assets/3e24dc3d-352b-4e7a-a1e5-d5d5c1a1a4f0" />


##  Query Table and Queries

### Query 1
    1. List customer name and average order amount 
<img width="1224" alt="424150567-5db1028f-1596-432b-89a8-cfd0219a1f9e" src="https://github.com/user-attachments/assets/776c6e71-4659-4f0b-b6da-dcaf305d4888" />

- Query 1 allows managers to see which customers are spending the most on average per order. This information can be very important in order to identify high-value customers who are notably contributing to our revenue. Through the calculation of each customer’s average order amount, managers would be able to send targeted promotions or exclusive offers. Managers would also be able to reward these customers with more loyalty points or give other perks. The results allows us to analyze customer spending behavior and identify customers based on their average spending amounts.

### Query 2
    2. List the employee ID, names, roles, and hire dates of employees who have worked at least 3 shifts in the past two weeks. The results should be sorted in ascending order by hire date to prioritize long-term employees.

<img width="1215" alt="424154494-864f677e-115a-465e-a121-4ed029703eb0" src="https://github.com/user-attachments/assets/8efcbfda-e283-4a06-8001-774916e52728" />


- Query 2 retrieves the employee ID, names, roles, and hire dates of employees who have worked at least three shifts in the past two weeks. By identifying active employees, managers can assess the workload distribution and ensure adequate staffing levels. Sorting the results in ascending order by hire date can be used to prioritize long-term employees, and allow managers to recognize and support experienced staff who consistently contribute to our business. This information can also help with scheduling decisions, ensuring that reliable employees are given appropriate opportunities based on their tenure and recent activity. 

### Query 3
    3. List all customers who are enrolled in the loyalty program who are from Gwinnett county and are of gold status 

<img width="1219" alt="424228390-a35046e7-37c3-4a7a-870f-9cc4a38289ff" src="https://github.com/user-attachments/assets/fc4380aa-d61b-4a3a-847f-3524ad970330" />

- Query 3 lists all customers who are enrolled in the loyalty program, are from Gwinnett County, and who have gold status. By analyzing these customers, managers can assess the potential demand for a second location in Gwinnett County. Our results have shown us that only three customers from Gwinnett County have reached gold status, which shows that we have a weaker customer base in this area. This suggests that it may not be a well-informed decision to open a second location in this area at this time. However, this data also gave us insight into the opportunity to implement targeted promotions and marketing efforts to strengthen our presence and expand our customer base in the area. 

### Query 4
    4. List the % of orders that have some type of croissant or a drink 
<img width="1199" alt="424187643-96bff709-5d87-422c-a3cb-96d39707961d" src="https://github.com/user-attachments/assets/6e76fae0-204d-4e4c-9128-7b2ace507529" />

- Query 4 calculates the percentage of total orders that have a type of croissant or a drink which would give managers information about our customers and their purchase patterns. This would help managers identify the demand for both croissants as well as drinks.  Our results show us that 34% of our orders include either a croissant or a drink. This percentage shows us that these are popular items on our menu. This information could be used to explore the potential opportunity of bundle deals or additional flavor options that could increase our profits.

### Query 5
    5. List the name of drivers, pickUpTime, deliveredTime, and rating if the driver is active
<img width="1125" alt="424160586-92bbb1e0-8beb-42e0-bb76-ecbd5f60c361" src="https://github.com/user-attachments/assets/77e00021-394f-43b8-ab1f-ecb37b566037" />

- Query 5 retrieves the names of active drivers, their pickup times, delivery completion times, and customer ratings by joining the DeliveryDriver and Delivery tables. This data allows managers to evaluate the performance of current active drivers by analyzing delivery efficiency and customer feedback. Reviewing customer ratings provides insight into our driver’s performance, which would show us our highly-rated drivers and those who may need further training or support. Our results have shown us that all of the drivers that are currently active have ratings that range from 4.5-4.9 stars. This demonstrates that overall, our drivers are consistently providing high-quality service, as reflected in their strong customer ratings

### Query 6
    6. List out ingredients that are being utilized in the bottom 25% from the orders placed 

<img width="1222" alt="424161589-33471393-63d0-4202-b8ca-d0bb7fc8945f" src="https://github.com/user-attachments/assets/67def91d-737a-4508-aede-26cafc750654" />

- Query 6 lists the ingredients that are being use in the bottom 25% of orders placed, providing managers with understanding which ingredients are used on a less frequent basis. A manager can make informed decisions about inventory management, product offerings, and possible menu adjustments. This can lead to item replacements, bringing new products to the business. This query helps ensure that inventory is enhanced and that ingredients are being used efficiently.

### Query 7
7. List which payment method generates the highest revenue, and what is its percentage of total payments

<img width="1216" alt="424163983-598a3619-648b-4a91-862f-e74d2cfcb14f" src="https://github.com/user-attachments/assets/fea133d6-3301-4f04-9f82-e404ab8f0e89" />

- Query 7 provides managers with useful information about how/what payment method is used to generate revenue. While credit card transactions are a major source of revenue, they can also come with processing fees of 1%-2%, impacting overall profitability. By understanding these uses of payment types, managers could try to promote payment methods like cash or even create giftcards to reduce transaction fees. Additionally, this information can be used to help negotiate better rates with card providers.

### Query 8
    8. List the orders where the total price of the items in the order exceeds the average price of all the items in that order.
    
<img width="1217" alt="424169943-31f565e7-5ca4-45cf-913d-08b5a71d0f20" src="https://github.com/user-attachments/assets/89ce9761-b7f2-4df6-b46b-e8dda8e708e1" />


- Query 8 is used to find the orders where the total cost of all items in the order is higher than the average price of the items in that order. This can be used to help managers see which orders have a higher price in purchases. This helps us understand our customer's spending habits, and make well informed decisions about pricing and the possibility of promotions. This also allows managers to identify which items contribute most to revenue and explore ways to enhance sales strategies for higher-priced products.


### Query 9 
    9. List menu items in order of most popular to least popular

<img width="1159" alt="424166749-a4f0805e-001c-41da-a1d1-ea8b4db1bd16" src="https://github.com/user-attachments/assets/83f64620-2709-4d0e-8369-6c103482fe9a" />

- Query 9 lists menu items in order of popularity, from most to least by counting how many times each item has been ordered. It assists managers identifying which items are the highest in demand, allowing them to focus on promoting these popular menu items, or adjust the menu based on customer preferences. By understanding the popularity of each item, managers can make  decisions about which items to remove, or improve to better meet our customer demand and improve overall sales performance.

### Query 10
    10. What time of day has the highest percentage of delivery orders

<img width="1213" alt="424168466-c9766674-b92e-4ae2-89c3-47c0c9ee2949" src="https://github.com/user-attachments/assets/3e77bea6-a7f1-408f-94b3-e2d12a9c22e5" />

- Query 10 determines which time of day has the highest percentage of delivery orders by comparing the number of delivery orders to the total number of orders at different times. It helps managers identify what are the peak delivery periods, which could help with staff assignments and utilizing inventory more effectively during these high-demand times. Looking into these delivery trends throughout the day can also show managers when they should consider offering promotions or discounts during slower times to increase profitability.


## Database Information

ns_Sp25_21479_Group4

Each query that is listed has been stored in the database using stored procedure through TP_Qx
