# Product Recommendation with Collaborative Filtering

## 1. Introduction

We have asked ourselves many times when shopping online, how do they know what we can buy? With this study we will try to understand the basics of 
recommendation systems. Aim is to defining two functions at the end, which recommends a product to the customer. One of them will be customer based 
and the other one will be item based.

## 2. Data

This is a transnational data set from [kaggle](https://www.kaggle.com/carrie1/ecommerce-data) which contains transactions mostly from wholesalers.

Field descriptions are below;

-InvoiceNo: Unique number of the invoice<br/>
-StockCode: Unique code of the product<br/>
-Description: Name of the product<br/>
-Quantity: The amount of the purchase<br/>
-InvoiceDate: Date of the invoice<br/>
-UnitPrice: Cost per product<br/>
-CustomerID: Unique ID of the customer<br/>
-Country: Location of the customer<br/>

## 3. Modelling

This model will be built on the **collaborative filtering** algorithm, which tries to answer the question; Do we have users that buy similar items? Let's 
say our system has records that we have a subset of users, who bought Metallica albums and most of these customers also bought Megadeath albums, too. 
Therefore, we can infer if someone purchases Metallica albums, they are also a likely candidate to purchase a Megadeath album. As can be seen from this 
example, that algorithm is used to recommend products based on the history of user behaviors and consequently looks at the similarites between users with 
a so called **user-to-item matrix**.

In user-to-item matrix, each row represents an individual customer and each column represents items in the inventory. In this case, 1 indicates that the 
customer purchased the relevant product, while 0 indicates the opposite. From this matrix, the similarity of customers will be calculated by 
using **cosine similarity** method to measure distance between customers.

<img src="image/formula.png" width="900" height="400">

