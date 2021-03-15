![](https://bn1305files.storage.live.com/y4mzAYxmbIIC_nmvccsxcMxIn078c3vVvo2hjmltqaoRhEtWlZnI3JdbZUICY8PZjRjDjzi6d47a7zaC2NaTN9AaLfskm8L0JfZYbvlVV9x9FK4MITpOUlH2De2JA_E0Cx8wETaL1rGxOma5KhqurIUC9RHIZDz5CTBIExxgZ37CNy0EUsamWWWsrg03qQy3hRe?width=369&height=137&cropmode=none)
# iamneo | Ecommerce | BookHub | Angular-Springboot-Fullstack-App


**Objective:**

BookHub is an online application to be built as a product that can be catering to various customers who requires purchasing books.

**Users of the System:**

1. Admin
2. Customer

**Functional Requirements:**

- Build an application that customer can access and purchase books online.
- The application should have signup, login, profile, dashboard page, and product page.
- This application should have a provision to maintain a database for customer information, order information and product portfolio.
- Also, an integrated platform required for admin and customer.
- Administration module to include options for adding / modifying / removing the existing product(s) and customer management.

While the above ones are the basic functional features expected, the below ones can be nice to have add-on features:

- Filters for products like Low to High or showcasing products based on the customer&#39;s price range, specific brands etc.
- Email integration for intimating new personalized offers to customers.
- Multi-factor authentication for the sign-in process
- Payment Gateway

**Output/ Post Condition:**

- Records Persisted in Success &amp; Failure Collections
- Standalone application / Deployed in an app Container

# Non-Functional Requirements:

| **Security** |
- App Platform –UserName/Password-Based Credentials
- Sensitive data has to be categorized and stored in a secure manner
- Secure connection for transmission of any data
 |
| --- | --- |
| **Performance** |
- Peak Load Performance (during Festival days, National holidays etc)
- eCommerce -\&lt; 3 Sec
- Admin application \&lt; 2 Sec
- Non Peak Load Performance
- eCommerce \&lt; 2 Sec
- Admin Application \&lt; 2 Sec
 |
 | --- | --- |
| **Availability** |
- 99.99 % Availability
 |
 | --- | --- |
| **Standard Features** |
- Scalability
- Maintainability
- Usability
- Availability
- Failover
 |
 | --- | --- |
| **Logging &amp; Auditing** |
- The system should support logging(app/web/DB) &amp; auditing at all levels
 |
 | --- | --- |
| **Monitoring** |
- Should be able to monitor via as-is enterprise monitoring tools
 |
 | --- | --- |
| **Cloud** |
- The Solution should be made Cloud-ready and should have a minimum impact when moving away to Cloud infrastructure
 |
 | --- | --- |
| **Browser Compatible** |
- IE 7+
- Mozilla Firefox Latest – 15
- Google Chrome Latest – 20
- Mobile Ready
 |
| --- | --- |
# Technology Stack
| --- | --- |
| Front End | Angular 7+Google Material Design Bootstrap / Bulma |
| --- | --- |
| Server Side | Spring BootSpring Web (Rest Controller)Spring SecuritySpring AOPSpring Hibernate |
| --- | --- | 
| Core Platform | OpenJDK 11 |
| --- | --- |
| Database | MySQL or H2 |
| --- | --- |

**Platform Pre-requisites (Do&#39;s and Don&#39;ts):**

1. The angular app should run in port 8081. Do not run the angular app in the port: 4200.
2. Spring boot app should run in port 8080.

**Key points to remember:**

1. The id (for frontend) and attributes(backend) mentioned in the SRS should not be modified at any cost. Failing to do may fail test cases.
2. Remember to check the screenshots provided with the SRS. Strictly adhere to id mapping and attribute mapping. Failing to do may fail test cases.
3. Strictly adhere to the proper project scaffolding (Folder structure), coding conventions, method definitions and return types.
4. Adhere strictly to the endpoints given below.

**Application assumptions:**

1. The login page should be the first page rendered when the application loads.
2. Manual routing should be restricted by using AuthGaurd by implementing the canActivate interface. For example, if the user enters as [http://localhost:4200/signup](http://localhost:4200/signup) or [http://localhost:4200/home](http://localhost:4200/home) the page should not navigate to the corresponding page instead it should redirect to the login page.
3. Unless logged into the system, the user cannot navigate to any other pages.
4. Logging out must again redirect to the login page.
5. To navigate to the admin side, you can store a user type as admin in the database with a username and password as admin.
6. Use admin/admin as the username and password to navigate to the admin dashboard.

**Validations:**

1. Basic email validation should be performed.
2. Basic mobile validation should be performed.

**Project Tasks:**

**API Endpoints:**

| USER |
 |
| --- | --- |
| Action | URL | Method | Response |
| --- | --- |
| Login | /login | POST | true/false |
| --- | --- |
| Signup | /signup | POST | true/false |
| --- | --- |
| Get All Products – Home | /home | GET | Array of Products |
| --- | --- |
| Add to cart | /home/{id} | POST | Item added to cart |
| --- | --- |
| Cart Items | /cart/{id} | GET | Array of Cart Items |
| --- | --- |
| Delete cart Item | /cart/delete | POST | Cart Deleted |
| --- | --- |
| Cart to Orders | /saveOrder | POST | Cart items added to the Orders list |
| --- | --- |
| Orders list | /orders | POST | Array of Orders |
| --- | --- |
| Place order directly | /placeOrder | POST | Place items to orders directly |
|
 |
 |
 |
 |
 | --- | --- |
| ADMIN |
| --- | --- |
 |
 |
 |
| Action | URL | Method | Response |
| Get All Products | /admin | GET | Array of Products |
| Add Product | /admin/addProduct | POST | Product added |
| Delete Product | /admin/delete/{id} | GET | Product deleted |
| Product Edit | /admin/productEdit/{id} | GET | Get All details of Particular id |
| Product Edit | /admin/productEdit/{id} | POST | Save the Changes |
| Get All Orders | /admin/orders | GET | Array of Orders |


**Frontend:**

**Customer:**

1. Signup: Design a signup page component where the new customer has options to sign up by providing their basic details.
  1. Ids:
    1. email
    2. username
    3. mobilenumber
    4. password
    5. confirmpassword
  2. API endpoint Url: [http://localhost:4200/signup](http://localhost:4200/signup)
  3. Output screenshot:

![](RackMultipart20210315-4-1qhju7z_html_6b2c7e20a0c6596.png)

1. Login: Design a login page component where the existing customer can log in using the registered email id and password.
  1. Ids:
    1. email
    2. password
  2. API endpoint Url: [http://localhost:4200/login](http://localhost:4200/login)
  3. Output screenshot:

![](RackMultipart20210315-4-1qhju7z_html_55316531e76633a6.png)

1. Dashboard / Home: Design a home page component that has the navigation bar and lists all the available products as grid elements with appropriate filter options.
  1. Ids:
    1. homeButton
    2. cartButton
    3. orderButton
  2. API endpoint Url: [http://localhost:4200/](http://localhost:4200/login)home
  3. Screenshot

![](RackMultipart20210315-4-1qhju7z_html_79ef20b65d997156.png)

1. Cart and Orders: Design a cart component and order component where we can see the cart items and see the items ordered after placing an order.
  1. Ids
    1. cartBody
    2. orderBody
  2. API endpoint Url: [http://localhost:4200/](http://localhost:4200/login)cart
  3. API endpoint Url: [http://localhost:4200/orders](http://localhost:4200/orders)
  4. Screenshot

![](RackMultipart20210315-4-1qhju7z_html_f436440e5177c99c.png)

**Admin:**

1. Admin Dashboard: Design a dashboard page where the list of products is displayed on the admin side.
  1. Ids
    1. addProduct
    2. productBody
  2. API endpoint Url: [http://localhost:4200/admin](http://localhost:4200/admin)
  3. Screenshot

![](RackMultipart20210315-4-1qhju7z_html_3e88f563434358f3.png)

1. Admin Navigation: Design a navigation component that can navigate to products and orders.
  1. Ids:
    1. adminOrderButton
    2. productButton
    3. logoutButton
  2. Screenshot:

![](RackMultipart20210315-4-1qhju7z_html_4af3fee3553adf00.png)

1. Add Product: Design an add product component in which the admin can add new products to the inventory.
  1. Ids:
    1. addProductBody
    2. productName
    3. productPrice
    4. description
    5. imageURL
    6. quantity
    7. addProductButton
  2. API endpoint Url: [http://localhost:4200/ad](http://localhost:4200/ad)dProduct
  3. Screenshot

![](RackMultipart20210315-4-1qhju7z_html_632b13862eabe81.png)

1. View Orders: Create a view component where the admin can look into the new and old orders.
  1. Ids:
    1. adminOrderBody
  2. API endpoint Url: [http://localhost:4200/admin](http://localhost:4200/admin)/orders
  3. Screenshot

![](RackMultipart20210315-4-1qhju7z_html_addf7d592975141c.png)

**Backend:**

**Class and Method description:**

**Model Layer:**

1. UserModel: This class stores the user type (admin or the customer) and all user information.
  1. Attributes:
    1. email: String
    2. password: String
    3. username: String
    4. mobileNumber: String
    5. active: Boolean
    6. role: String
    7. cart: CartModel
    8. ordersList: List\&lt;OrderModel\&gt;
  2. Methods: -
2. LoginModel: This class contains the email and password of the user.
  1. Attributes:
    1. email: String
    2. password: String
  2. Methods: -
3. ProductModel: This class stores the details of the product.
  1. Attributes:
    1. productId: String
    2. imageUrl: String
    3. productName: String
    4. price: String
    5. description: String
    6. quantity: String
  2. Methods: -
4. CartModel: This class stores the cart items.
  1. Attributes:
    1. cartItemID: String
    2. userId: UserModel
    3. ProductName: String
    4. Quantity: int
    5. Price: String
  2. Methods: -
5. OrderModel: This class stores the order details.
  1. Attributes:
    1. orderId: String
    2. userId: String
    3. ProductName: String
    4. quantity: int
    5. totalPrice: String
    6. Status: String
    7. Price: String
  2. Methods: -

**Controller Layer:**

1. SignupController: This class control the user signup
  1. Attributes: -
  2. Methods:
    1. saveUser(UserModel user): This method helps to store users in the database and return true or false based on the database transaction.
2. LoginController: This class controls the user login.
  1. Attributes: -
  2. Methods:
    1. checkUser(LoginModeldata): This method helps the user to sign up for the application and must return true or false
3. ProductController: This class controls the add/edit/update/view products.
  1. Attributes: -
  2. Methods:
    1. List\&lt;ProductModel\&gt;getProduct(): This method helps the admin to fetch all products from the database.
    2. List\&lt;ProductModel\&gt;getHomeProduct(): This method helps to retrieve all the products from the database.
    3. ProductModelproductEditData(Stringid): This method helps to retrieve a product from the database based on the productid.
    4. productEditSave(ProductModeldata): This method helps to edit a product and save it to the database.
    5. productSave(ProductModeldata): This method helps to add a new product to the database.
    6. productDeleteStringid): This method helps to delete a product from the database.
4. CartController: This class helps in adding product to the cart, deleting the products from the cart, updating items in the cart.
  1. Attributes: -
  2. Methods:
    1. addToCart(StringQuantity, Stringid): This method helps the customer to add the product to the cart.
    2. List\&lt;CartTempModel\&gt;showCart(Stringid): This method helps to view the cart items.
    3. deleteCartItem(Stringid): This method helps to delete a product from the cart.
5. OrderController: This class helps with the orders such as save order/ place an order/ view order.
  1. Attributes: -
  2. Methods:
    1. List\&lt;OrderTemp\&gt;getUserProducts(Stringid): This method helps to list the orders based on the user id.
    2. saveProduct(Stringid): This method helps to save the cart items as an order.
    3. placeOrder(OrderModelorder): This method helps to place an order by the customer.
