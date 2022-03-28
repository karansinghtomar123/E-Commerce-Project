# E-Commerce-Project

## (Using Angular &amp; ASP.NET)

This project deals with developing a Virtual website ‘E-commerce Website’. It provides the user with a list of the various products available for purchase in the store. For the convenience of online shopping, a shopping cart is provided to the user. After the selection of the goods, it is sent for the order confirmation process. The system is implemented using ASP.net and Angular. To develop an e-commerce website, it is necessary to study and understand many technologies.

### Scope:

The scope of the project will be limited to some functions of the e-commerce website. It will display products, customers can select catalogs and select products, and can remove products from their cart specifying the quantity of each item. Selected items will be collected in a cart. At checkout, the item on the card will be presented as an order. Customers can pay for the items in the cart to complete an order. This project has great future scope. The project also provides security with the use of login ID and passwords, so that no unauthorized users can access your account. The only authorized person who has the appropriate access authority can access the software.

# E-Commerce Life Cycle

1. Plan
2. Analysis
3. Design
4. Development
5. Test
6. Implement
7. Maintain

# SDLC Model Used

## Iterative & Incremental Model

The Iterative & Incremental SDLC model essentially brings together an iterative design with an incremental development model which makes it amongst the best SDLC methodology for business.

# Technologies Used

1. Frontend: Angular 12
2. Backend: ASP.NET Core Web API - .NET 5

# Home Page
![image](https://user-images.githubusercontent.com/31335553/160286240-b944fda1-3d8b-4be8-8f50-f8cd66f365f4.png)

# Item Detail Page
![image](https://user-images.githubusercontent.com/31335553/160286298-a69f1ba7-10ff-4690-a7ee-2b1fc2d64cf6.png)

# Shopping Cart
![image](https://user-images.githubusercontent.com/31335553/160286348-bfe1381c-a043-4f56-99ab-3054ad356700.png)

# Schema
![image](https://user-images.githubusercontent.com/31335553/160286581-e8b41476-cb40-4d3e-86f8-cb123132ed88.png)

# Flowchart
![image](https://user-images.githubusercontent.com/31335553/160286620-e86881e3-6503-4c36-994a-31f450dd7efd.png)

# DB Query

CREATE TABLE [dbo].[cart_item] (
[Id] INT NOT NULL,
[session_id] INT NOT NULL,
[product_id] INT NOT NULL,
[quantity] INT NOT NULL,
[created_at] ROWVERSION NOT NULL,
PRIMARY KEY CLUSTERED ([Id] ASC)
);


CREATE TABLE [dbo].[discount] (
[Id] INT NOT NULL,
[name] VARCHAR (50) NOT NULL,
[desc] TEXT NOT NULL,
[discount_percent] DECIMAL (18) NOT NULL,
[created_at] ROWVERSION NOT NULL,
PRIMARY KEY CLUSTERED ([Id] ASC)
);


CREATE TABLE [dbo].[order_details] (
[Id] INT NOT NULL,
[user_id] VARCHAR (50) NOT NULL,
[total] DECIMAL (18) NOT NULL,
[payment_id] INT NOT NULL,
[created_at] ROWVERSION NOT NULL,
PRIMARY KEY CLUSTERED ([Id] ASC)
);


CREATE TABLE [dbo].[order_items] (
[Id] INT NOT NULL,
[order_id] INT NOT NULL,
[product_id] INT NOT NULL,
[created_at] ROWVERSION NOT NULL,
PRIMARY KEY CLUSTERED ([Id] ASC)
);


CREATE TABLE [dbo].[payment_details] (
[Id] INT NOT NULL,
[order_id] INT NOT NULL,
[amount] INT NOT NULL,
[provider] VARCHAR (1) NOT NULL,
[status] VARCHAR (1) NOT NULL,
[created_at] ROWVERSION NOT NULL,
PRIMARY KEY CLUSTERED ([Id] ASC)
);


CREATE TABLE [dbo].[product] (
[Id] INT NOT NULL,
[name] VARCHAR (50) NOT NULL,
[desc] TEXT NOT NULL,
[SKU] VARCHAR (50) NOT NULL,
[category] VARCHAR (50) NOT NULL,
[price] DECIMAL (18) NOT NULL,
[discount_id] INT NOT NULL,
[created_at] ROWVERSION NOT NULL,
PRIMARY KEY CLUSTERED ([Id] ASC)
);


CREATE TABLE [dbo].[product_type] (
[Id] INT NOT NULL,
[Women's] VARCHAR (50) NOT NULL,
[Men] VARCHAR (50) NOT NULL,
[Kid] VARCHAR (50) NOT NULL,
[Electronic Devices] VARCHAR (50) NOT NULL,
PRIMARY KEY CLUSTERED ([Id] ASC)
);


CREATE TABLE [dbo].[user] (
[Id] INT NOT NULL,
[username] VARCHAR (50) NOT NULL,
[password] TEXT NOT NULL,
[first_name] VARCHAR (50) NOT NULL,
[last_name] VARCHAR (50) NOT NULL,
[address] VARCHAR (50) NOT NULL,
[telephone] INT NOT NULL,
[created_at] ROWVERSION NOT NULL,
PRIMARY KEY CLUSTERED ([Id] ASC)
);





