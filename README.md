Assignment I – Windows Functions

MY NAME IS URUMURI GASANA M NOELLA am AUCA student in IT(software engineering)

why i choise this is becouse I did my internship at NAEB (National Agricultural Export Development Board). NAEB helps farmers sell coffee and other crops. The cooperative collects a lot of sales data from markets across Rwanda. This project uses that data to help NAEB and local farmers make better choices.

Data challenge

NAEB gets many sales records from farmers, buyers, and markets. It is hard to:

see which farmers sell the most,

know which products sell best in each district,

find months with high or low sales.

We need simple reports so managers can act quickly.

Expected outcome

From the data we will find:

the top 5 farmers in each district every month,

which products sell best in each place,

monthly revenue trends (money going in),

groups of buyers by how much they spend,

3-month moving averages to see short trends.

This helps NAEB plan training, buy/export decisions, and support farmers.

Success criteria — 5 clear goals

Top 5 farmers by month and district — use RANK() to find winners.

Running monthly revenue per district — use SUM() OVER() to track total money over time.

Month-over-month growth per district — use LAG() to compare this month with last month.

Buyers split into 4 groups by spending — use NTILE(4) to find top buyers and small buyers.

3-month moving average of monthly sales — use AVG() OVER(...) to smooth the data.

Database schema (ER)

We make 4 tables:

FARMERS: farmer_id, name, district

BUYERS: buyer_id, name, type (wholesale/retail), district

PRODUCTS: product_id, name, category (coffee/maize/veg)

TRANSACTIONS: transaction_id, buyer_id, product_id, farmer_id, market, transaction_date, amount

This structure lets us link each sale to a farmer, buyer, product and place.

FARMERS 1 ---< TRANSACTIONS >--- 1 PRODUCTS
>--- 1 BUYERS

How this helps people

Farmers: they see when and where their crops sell best. They get advice to grow more of what sells.

NAEB managers: they know which districts need support and where to promote exports.

Buyers/exporters: they find reliable farmers and plan purchases.

Local markets: they can plan stock and staff for busy months.

Small cooperatives: they get evidence to ask for loans or help from NAEB.
