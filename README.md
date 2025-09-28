![WhatsApp Image 2025-09-28 at 15 08 03_c93a4e6b](https://github.com/user-attachments/assets/9dd7b8c7-e431-485f-b50b-956c96fcc7c8)
📂 Project Structure

data/ → Contains the dataset used for analysis (CSV/Excel).     
Exploratory Data Analysis.ipynb → Initial data cleaning and exploration.     
vendor performance analysis.ipynb → Detailed vendor performance analysis with Python (Pandas, Matplotlib, Seaborn).    
get_vendor_summary.py → Script to generate vendor summary reports.        
vendor performance.pbix → Power BI dashboard for interactive visualization     

🧭 Motivation & Goals

To monitor and measure vendor performance across different dimensions (e.g. delivery time, quality, cost, reliability)     
To surface insights and trends that help business stakeholders make data-driven decisions      
To build an interactive dashboard for stakeholder usage     

🛠️ Technologies & Tools Used
Python (pandas, numpy, matplotlib, seaborn, etc.)      
Jupyter Notebooks     
Power BI (for visualization & dashboarding)     
Git for version control   

Business Problem

Effective inventory and sales management are critical for optimizing profitability in the retail and wholesale industry. Companies need to ensure that they are not incurring losses due to inefficient pricing, poor inventory turnover, or vendor dependency. The goal of this analysis is to:

	Identify underperforming brands that require promotional or pricing adjustments.   
	Determine top vendors contributing to sales and gross profit.     
	Analyze the impact of bulk purchasing on unit costs.     
	Assess inventory turnover to reduce holding costs and improve efficiency.    
	Investigate the profitability variance between high-performing and low-performing vendors.   

<img width="731" height="474" alt="Screenshot (21)" src="https://github.com/user-attachments/assets/e7bc5af4-6809-4986-a866-60b00c962b9a" />

<img width="1268" height="853" alt="image1" src="https://github.com/user-attachments/assets/33a28015-b324-4574-b540-df265fdad8f2" />




Negative & Zero Values:
Gross Profit: Minimum of -52,002.78, indicating potential losses due to high costs or heavy discounts. This could be due to selling products at lower prices than their purchase costs.

Profit Margin: Has a minimum of -∞, which suggests instances where revenue is zero or even lower than the total cost, leading to extreme negative profit margins.

Total Sales Quantity & Sales Dollars: Some products show zero sales, indicating they were purchased but never sold. These may be slow-moving or obsolete stock, leading to inventory inefficiencies.

Outliers Detected by High Standard Deviations:
Purchase & Actual Prices: The maximum values (5,681.81 & 7,499.99)

Freight Cost: Extreme variation from 0.09 to 257,032.07 suggests logistics inefficiencies, bulk shipments, or erratic shipping costs across different products.

Stock Turnover: Ranges from 0 to 274.5, suggesting some products sell rapidly while others remain unsold for long periods. A value greater than 1 indicates that sales for a product exceed the purchased quantity due to older stock fulfilling orders.

Dta filtering:
To enhance the reliability of the insights , we removed inconistent data points where:
•	Gross profit <= 0 (to exclude transactions leading to losses).
•	Profit margin<=0(to ensure analysis focuses on profitable transactions).
•	Total sales quantity=0(to eliminate inventory that was never sold)

CORRELATION INSIGHTS
<img width="1054" height="826" alt="image 2" src="https://github.com/user-attachments/assets/8ea2da76-5e04-4a8e-968f-c7187dde2741" />


Purchase price VS Total sales dollar and Gross profit:  Week correlation (-0.012 and-0.016) ,indicating that price variation do not significantly impact sales revenue or profit.
Total purchase quantity VS Total sales quantity: Strong correlation (0.999) , confirming efficient inventory turnover.
Profit margin VS Total sales price: Negative correlation (-0,179), suggesting increasing sales price may lead to reduced margins, possibly due to competitive pricing pressure.
Stock turnover VS Gross profit & Profit margin: weak negative correlation ,indicating that faster stock turnover does not necessarily equate to higher profitability.


Research questions and key findings
Brands for promotional or pricing adjustments
<img width="421" height="550" alt="Screenshot (20)" src="https://github.com/user-attachments/assets/713a9e6d-2881-4069-acaa-28005652ba3d" />

These brand exhibit lower sales but higher progit margins, which could benefit from targeted marketing, promotions or price optimization to increase volume without compromising profitability.

POWER BI DASHBOARD
<img width="906" height="504" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/42956c95-087b-4a5a-b655-2d6d2e1d00f0" />



