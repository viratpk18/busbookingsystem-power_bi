# busbookingsystem-power_bi
Online Bus Booking System Using Power BI
1.Instruction
An Online Bus Ticket Booking System enables passengers to book bus tickets online for various routes. The system allows users to select buses, choose their seats, and make payments. This document explains how data for such a system is structured in Excel and visualized using Power BI.

2. Data Structure
The data is divided into four primary datasets:
Bus Details
Customer Details
Booking Details
Payment Details
These datasets are interconnected, forming the backbone of the ticket booking system.

2.1. Bus Details Table
Stores information related to the buses operating in the system.

Column Name	Data Type	Description
Bus_ID	Integer	Unique identifier for each bus
Bus_Number	Text	The bus number (license plate)
Route	Text	The route the bus operates on (e.g., City A - City B)
Departure_Time	Time	Time of departure
Arrival_Time	Time	Time of arrival
Seats_Available	Integer	Number of seats available for booking
Price	Currency	Price per seat
2.2. Customer Details Table
Contains details of customers using the system.

Column Name	Data Type	Description
Customer_ID	Integer	Unique identifier for each customer
Name	Text	Full name of the customer
Email	Text	Customer’s email address
Phone	Text	Customer’s phone number
2.3. Booking Details Table
Holds information about each ticket booking.

Column Name	Data Type	Description
Booking_ID	Integer	Unique booking identifier
Bus_ID	Integer	Reference to the bus being booked
Customer_ID	Integer	Reference to the customer making the booking
Booking_Date	Date	Date when the booking was made
Seats_Booked	Integer	Number of seats booked by the customer
Total_Price	Currency	Total price for the booking
2.4. Payment Details Table
Records payment information for bookings made.

Column Name	Data Type	Description
Payment_ID	Integer	Unique identifier for the payment
Booking_ID	Integer	Reference to the related booking
Payment_Date	Date	Date of payment
Payment_Amount	Currency	Amount paid
Payment_Status	Text	Status of payment (Paid/Pending)
3. Power BI Integration
The Excel datasets are imported into Power BI to create visualizations and generate insights from the booking data. Below are the steps for creating dashboards and visualizations in Power BI.

3.1. Import Data from Excel
Open Power BI Desktop.
Go to Home > Get Data > Excel.
Select the Excel file containing the datasets (Bus Details, Customer Details, Booking Details, Payment Details).
Load the data into Power BI.
3.2. Establish Relationships
Navigate to the Model View.
Establish relationships between the tables based on the primary keys:
Bus_ID (in Booking Details) connects to Bus_ID (in Bus Details).
Customer_ID (in Booking Details) connects to Customer_ID (in Customer Details).
Booking_ID (in Payment Details) connects to Booking_ID (in Booking Details).
This creates the relationships necessary for cross-referencing between buses, customers, and payments.

4. Visualizations
4.1. Booking Summary Dashboard
Table/Matrix Visualization: Displays a summary of bookings including:
Booking Date
Bus Route
Seats Booked
Total Price
4.2. Revenue Analysis
Card Visualization: Shows total revenue generated from all bookings.
Bar Chart: Compares total revenue across different bus routes.
Pie Chart: Displays revenue distribution per customer.
4.3. Seat Availability
Gauge Chart: Tracks the available seats for each bus in real time.
4.4. Payment Status
Stacked Column Chart: Shows the distribution of Paid vs. Pending payments.

5. Advanced Features
5.1. Filters and Slicers
Date Filters: Allows filtering data by booking or payment date.
Bus Route Filter: Enables filtering by specific bus routes.
Customer Filter: Displays data for specific customers.
5.2. Scheduled Refresh
Set up a scheduled refresh to update Power BI data automatically as the Excel file is updated.

6. Conclusion
This Bus Ticket Booking System integrates Excel datasets and Power BI to create a comprehensive, user-friendly dashboard for managing and analyzing bookings, customers, and payments. The Power BI visualizations help stakeholders track key metrics, monitor seat availability, and ensure smooth payment processing.
