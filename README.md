# ☕ Les Maisons Café Management System - University Case Study  

![ERD Diagram](erd-diagram.png) *<!-- Replace with your actual ERD image -->*  

[![Database: SQL Server](https://img.shields.io/badge/Database-SQL%20Server-orange)](https://www.microsoft.com/en-us/sql-server)  
[![Backend: Python](https://img.shields.io/badge/Backend-Python%203.10-blue)](https://www.python.org/)  
[![Design: 3NF](https://img.shields.io/badge/Design-3NF%20Normalized-brightgreen)](https://en.wikipedia.org/wiki/Third_normal_form)  
[![BI: Power BI](https://img.shields.io/badge/BI-Power%20BI-yellow)](https://powerbi.microsoft.com/)  
[![API: FastAPI](https://img.shields.io/badge/API-FastAPI-green)](https://fastapi.tiangolo.com/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-blue)](https://opensource.org/licenses/MIT)  

## 📌 **Business Case Study: Optimizing Café Operations**  

### **Challenge**  
Les Maisons café chain faced:  
- 30% inventory waste from poor forecasting  
- 15% loyalty program fraud incidents  
- No centralized event performance tracking  

### **Tech-Driven Solution**  
| Component | Technology | Implementation |  
|-----------|------------|----------------|  
| **Database** | SQL Server 2019 | 3NF-compliant schema with 15+ tables |  
| **Backend** | Python 3.10 | FastAPI microservices |  
| **Analytics** | Power BI | Real-time dashboards |  
| **ETL** | Azure Data Factory | Daily data pipelines |  
| **Version Control** | Git/GitHub | CI/CD workflows |  

## 🏗️ **Database Architecture**  

### **Core Modules**  
```bash
erDiagram
    CUSTOMERS ||--o{ ORDERS : "places"
    ORDERS ||--|{ ORDER_ITEMS : "contains"
    INVENTORY }|--|| PRODUCTS : "tracks"
    EVENTS ||--o{ PROMOTIONS : "triggers"
    LOYALTY ||--o{ REDEMPTIONS : "processes"
```
heatmaps

🚀 Implementation Highlights
```
-- Sample Stored Procedure
CREATE PROCEDURE CalculateLoyaltyPoints
    @CustomerID INT,
    @OrderAmount DECIMAL(10,2)
AS
BEGIN
    UPDATE LoyaltyAccounts
    SET Points = Points + (@OrderAmount * 0.1)
    WHERE CustomerID = @CustomerID
END
```
