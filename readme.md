## Description

This project is an application built to manage **E-Commerce Fashion categories** in a tree structure, where categories can have multiple levels of subcategories. The app supports CRUD operations for these categories and can display them in a hierarchical (tree) view.

## Problem Statement:

Build an API that can manage fashion categories with unlimited depth. 
The application should allow creating, updating, deleting, and displaying categories in a tree structure.

Sample Data:    

	-Women
		- Clothing
			- Dresss
				- Causal Dresses
				- Party Dresses
		- T-Shirts
			- Printed T-shirts
			- Causal T-Shirts
			- Plain T-Shirts
	-Men
		- Footwear
			- Branded
			- Non Branded
		- T-Shirts
			- Printed T-shirts
			- Causal T-Shirts
			- Plain T-Shirts
		- Shirts
			- Party Shirts
			- Causal Shirts
			- Plain Shirts

## Tasks

	1. Design an API that displays categories in a hierarchical tree view with N levels.
	2. Provide API endpoints to **create**, **update**, and **delete** categories.
	3. Display the categories in a tree structure.

## Requirements

	- Follow typical **RESTful API** design patterns.
	- Data should be stored in the **MongoDB** database.

## Installing Dependencies

```bash
$ npm install
```

## Running The App

```bash
# production mode
npm start

# development mode
npm run dev
```

## Running Test Cases

```bash
npm run test
```
   
## cURLs

1.  Add New Category [POST]

```bash
	curl --location 'localhost:3088/category' \
	--header 'Content-Type: application/json' \
	--data '{
		"name": "Plain T-Shirts",
		"parent": "65f1ad0144b738e90a6dd517"
	}'
```

2. List Categories [GET]
    
```bash
	curl --location 'localhost:3000/categories?depthLevel=4&limit=2'
```

3. Update Category [PUT]
        
```bash
   curl --location --request PUT 'localhost:3088/category/65f27a895cd1f5a22e3e8b19' \
	--header 'Content-Type: application/json' \
	--data '{
		"name": "Plain T-Shirts - update",
		"parent": "65f1ad0144b738e90a6dd517"
	}'
```

3. Delete Category [PUT]

```bash
	curl --location --request DELETE 'localhost:3000/category/65f1b35f1083a004ad2158ca'
```

## Category Collection View

    https://github.com/dibyenduswar/E-Commerce-Fashion-Category-Management-API-with-Nested-Hierarchical-Structure/blob/master/img/mongo-table-data.png

![alt text](https://github.com/dibyenduswar/E-Commerce-Fashion-Category-Management-API-with-Nested-Hierarchical-Structure/blob/master/img/mongo-table-data.png)
    
## Category List View

    https://github.com/dibyenduswar/E-Commerce-Fashion-Category-Management-API-with-Nested-Hierarchical-Structure/blob/master/img/category-list-view.png

![alt text](https://github.com/dibyenduswar/E-Commerce-Fashion-Category-Management-API-with-Nested-Hierarchical-Structure/blob/master/img/category-list-view.png)

## Stay in touch

- Author - Dibyendu Swar
- LinkedIn - [https://www.linkedin.com/in/dibyendu-swar/]

## Note
1.  For simplicity, all code is contained within a single JavaScript file.
2.  Request validation is omitted for simplicity. In a production environment, it's essential to include proper request validation.
3.  Environment variables or a secret manager should be used to securely store sensitive information like the MongoDB URI. 
