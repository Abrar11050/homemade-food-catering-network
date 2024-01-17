# CaterNet - Homemade Food Catering Network

## Description

I made this MERN-stack based application a long ago back in undergrad. It was lying in my old laptop neglected so I decided to push it here. It was made during my early days of React journey so the FE isn't very well built :P

Anyway, the idea of this comes from online food ordering platforms. Unlike more established platforms out there, this thing focuses only on independent vendors running homemade food business, no restaurant or big food-chains welcome here.

Please note that as it was a demo showcasing app, the user registration doesn't have email verification feature. Also, the payment info in food ordering is a placeholder, so ordering relies on manual cash-on-delivery.

![page slides](/repo-images/page_slides.gif "Page Slides")

## Features

* Registering as either customer/vendor/deliveryperson
* Vendor can create storefronts specifying name, title, tags, icon image, banner images, pickup locations.
* Each storefront can have multiple pickup locations.
* Vendor can add products to a storefront specifying product name, desc, tags, price, availability, and slideshow images.
* Vendor can monitor the orders under a storefront, as well as reviews and reports.
* Customers can search for products, or storefronts.
* Customers can go to storefront pages and view list of products.
* Customers can go to individual product pages via storefront's product list, or directly from search results.
* Product pages show product details, including product image slideshow.
* Customers can order a specific product by specifying quantity, and delivery location.
* Deliveryperson can find new delivery orders from the task finder.
* All parties can update an order's state depending on their role and the order's current state *(example: ordered/prepared/shipped/on-delivery/handed)*
* Customers can drop public reviews under storefronts, or file private reports.

## Running

In the local machine configuration, the react pages are served using the same server the backend api run on. As for such, the react build output directory is copied upon build. You don't have to manually copy/move it, the provided does it automatically for you.

Run the build script first (only needed to be run once):

```bash
./build.ps1 # If you're on Windows

# Or

./build.sh # If you're on Linux
```

You must specify these global variables:

* ``DBLINK`` specifying url **(including database name)** to a running MongoDB instance. If the instance is on localhost, prefer writing ``0.0.0.0`` instead of ``localhost`` to avoid MongoClient connection errors.
* ``JWT_SECRET`` specifying the JWT secret string.
* ``PORT`` specifying the port to run the server on.

Then run the server:

```bash
./run.ps1 # If you're on Windows

# Or

./run.sh # If you're on Linux
```

Frontend is based on [Zay Shop Template](https://themewagon.com/themes/free-bootstrap-5-html-5-ecommerce-website-template-zay-shop/)
