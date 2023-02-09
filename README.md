# e-Commerce-DBMS

A short description of the project.  
The E-Commerce enterprise consists of  a variety of products which are offered to the consumers in affordable prices and great quality. 
The Customers can buy this products in store physically, online with a user friendly interface or with our door to door services. 
Also some features included are different payment methods such as Credit Card, paypal or bank transfer. 
Being able to track the shipment of the customers product. 
Being able to log in or sign up. 
Being able to leave reviews about specific product with ratings from 1 to 5. 


The Relationships between the Entities:
1.Customer: 
One-to-Many relationship between Customer and Order (a customer can place multiple orders). 
One-to-Many relationship between Customer and Shipping Address (a customer can have multiple shipping addresses). 
One-to-Many relationship between Customer and Payment Method (a customer can have multiple payment methods). 
One-to-One relationship between Customer and Cart (a customer can have only one active cart at a time). 
One-to-Many relationship between Customer and Review (a customer can write multiple reviews).
2.Order: 
One-to-Many relationship between Order and Order Item (an order can contain multiple items). 
Many-to-One relationship between Order and Customer (an order must be placed by a customer). 
Many-to-One relationship between Order and Shipping Address (an order can only have one shipping address). 
Many-to-One relationship between Order and Payment Method (an order can only have one payment method). 
Many-to-One relationship between Order and Tax (an order can have only one tax applied).
3.Product: 
Many-to-Many relationship between Product and Category (a product can belong to multiple categories, and a category can contain multiple products). 
Many-to-One relationship between Product and Vendor (a product can have only one vendor). 
One-to-Many relationship between Product and Product Image (a product can have multiple images). 
One-to-Many relationship between Product and Review (a product can have multiple reviews). 
Many-to-Many relationship between Product and Coupon (a product can be eligible for multiple coupons, and a coupon can be applied to multiple products). 
Many-to-Many relationship between Product and Wishlist (an item can be added to a wishlist at any time, and a customer can have multiple wishlists). 
Many-to-Many relationship between Product and Cart (an item can be added to a cart at any time, and a customer can have only one active cart). 
4.Category:  
Many-to-Many relationship between Category and Product (a product can belong to multiple categories, and a category can contain multiple products).
5.Payment Method: 
Many-to-One relationship between Payment Method and Customer (a payment method must belong to a customer). 
6.Cart:  
One-to-One relationship between Cart and Customer (a customer can have only one active cart at a time). 
Many-to-Many relationship between Cart and Product (an item can be added to a cart at any time, and a customer can have only one active cart). 
7.Review:  
Many-to-One relationship between Review and Customer (a review must be written by a customer). 
Many-to-One relationship between Review and Product (a product can have multiple 
8.Order Item: 
Many-to-One relationship between Order Item and Order (an order item must belong to an order). 
Many-to-One relationship between Order Item and Product (an order item must be for a specific product). 
9.Vendor: 
One-to-Many relationship between Vendor and Product (a vendor can have multiple products). 
10.Product Image: 
Many-to-One relationship between Product Image and Product (an image must belong to a product). 
11.Coupon: 
Many-to-Many relationship between Coupon and Product (a product can be eligible for multiple coupons, and a coupon can be applied to multiple products). 
12.Shipment:  
Many-to-One relationship between Shipment and Order (a shipment must be for a specific order). 
13.Shipping Address: 
Many-to-One relationship between Shipping Address and Customer (a shipping address must belong to a customer). 
14.Product coupon: 
One coupon can be applied to multiple products (Many-to-One). 
One product can have multiple coupons (One-to-Many). 
15.Product cart: 
One-to-Many relationship between Customer and Product Cart, where a customer can have many product carts, but each product cart belongs to one customer. 
Many-to-Many relationship between Product and Product Cart, where a product can belong to many product carts, and each product cart can have many products. 
One-to-One relationship between Product Cart and Order, where a product cart can result in one order and an order can be linked to one product cart. 
One-to-Many relationship between Coupon and Product Cart, where a coupon can be applied to many product carts, but each product cart can have only one coupon. 
Many-to-One relationship between Payment Method and Product Cart, where a product cart can have only one payment method, but a payment method can be used for many product carts. 
16.product category: 
One-to-many relationship between category and product category, where one category can have many product category records. The foreign key in the product category table would reference the primary key in the category table. 
Many-to-one relationship between product and product category, where many product records can be associated with one product category record. The foreign key in the product category table would reference the primary key in the product table. 




THE BUSINESS RULES.  
1.Customer: 
A customer must provide a unique email address when creating an account. 
A customer must provide a password when creating an account. 
A customer must provide a billing address when making a purchase. 
A customer's personal information can be updated at any time. 
2.Order: 
An order must be placed by a customer. 
An order must contain at least one item.
An order must have a unique order number.
An order can only have one shipping address. 
An order can only have one payment method. 
3.Product: 
A product must have a unique product ID. 
A product must belong to at least one category. 
A product must have a name, description, and price. 
The price of a product can be updated at any time. 
4.Category: 
A category must have a unique category ID. 
A category must have a name. 
A product can belong to multiple categories.
5.Shipping Address: 
A shipping address must belong to a customer. 
A customer can have multiple shipping addresses.
6.Payment Method: 
A payment method must belong to a customer. 
A customer can have multiple payment methods. 
A payment method must have a unique payment method ID. 
7.Cart: 
A cart must belong to a customer. 
A customer can have only one active cart at a time. 
An item can be added to a cart at any time. 
An item can be removed from a cart at any time.
8.Product Category: 
A product can belong to multiple categories. 
A category can contain multiple products. 
When a product is deleted, its association with categories is also deleted. 
When a category is deleted, its association with products is also deleted 
9.Review: 
A review must be written by a customer. 
A product can have multiple reviews. 
A customer can write multiple reviews. 
A review must have a rating (e.g. 1-5 stars).
10.Product Coupon: 
A product can have multiple coupons associated with it.
A coupon can be associated with multiple products.. 
A product coupon association can be limited to a certain number of uses. 
The discount applied by a coupon to a product can be a fixed amount or a percentage of the product's price. 
A product coupon association can only be used once per order. 
11.Coupon: 
A coupon can be applied to multiple products. 
A product can be eligible for multiple coupons. 
A coupon must have a unique coupon code. 
A coupon has a start and end date. 
12.Vendor: 
A product can have only one vendor. 
A vendor can sell multiple products. 
13.Customer Address: 
Each customer can have multiple addresses (ex. billing and shipping addresses). 
A customer address must be associated with a customer. 
An address cannot be used by multiple customers. 
An address must have a unique identifier (address ID). 
An address must have accurate information such as street address, city, state/province, zip/postal code, and country. 
An address must have a valid format for the specific country it is located in. 
14.Order Item: 
An order item must belong to an order. 
An order can contain multiple order items. 
An order item must have a unique item ID. 
An order item must have a product ID. 
An order item must have a quantity. 
15.Product Image: 
A product image must belong to a product. 
A product can have multiple images. 
A product image must have a unique image ID 
16.Product Cart: 
A product can be in multiple carts. 
A cart can contain multiple products. 
The quantity of a product in a cart can be updated. 
A product can be removed from a cart. 
The total price of a cart is calculated based on the quantity of products in the cart and their individual prices.
