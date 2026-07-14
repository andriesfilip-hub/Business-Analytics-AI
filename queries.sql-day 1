-- ========================================
-- SQL Practice: Bank Customer Churn Dataset
-- ========================================

--1. Total number of customers in the dataset
SELECT COUNT(*) AS Total_Customers
FROM Customers;

--2. Churn rate based on gender
SELECT Gender, 
       COUNT(*) AS Total,
       SUM(Existed) AS Churned,
       ROUND(SUM(Existed) * 100.0 / COUNT(*), 2) AS Churn_Rate_Percentage
FROM Customers
GROUP BY Gender;

--3. Clients who remained vs. clients who churned
SELECT Exited, 
       AVG(Balance) AS Average_Balance,
FROM Customers
GROUP BY Exited;
