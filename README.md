ColdIgniter
============
by Simplifie

Inspired by my lazy self. Includes simple features to make developers more productive by speeding up workflow and meet deadlines that were missing in CodeIgniter 2.1.0.

- Generate easy CRUDs with simple commands. See application/controllers/g.php

- Foundation Framework 5 for responsive layout (Cold Foundation)

- See application/helpers for the list of Helpers including CSV generator
- See public/js/fb.js for easy Facebook integration. See $(document).ready() for a one-liner implementation of custom Facebook button
- See application/views/generators/auth for basic Auth files such as login and register
- PayPal
  - Refer to libraries/sparks/payments
	- Basic payments using DirectPayment and ExpressCheckout
	- Recurring payment to be included
    - http://tareqalam.com/2010/07/07/paypal-recurring-payment-integrated-with-codeigniter/
    - http://ci-merchant.org/
    - http://stackoverflow.com/questions/21846374/recurring-payment-in-paypal-with-codeigniter-website
- More CRUD commands and properties to be included
	- generate crud employee id:int linked_to:user
    - linked_to:user
			- Generates an indexed user_id in the DB to be used as foreign key
			- Generates a hidden tag in the update view (Not yet implemented)
- AJAX MailChimp to be included

- Libraries:
  - Root folders should be in plural, all lower case
  - Underscore separator only
  - Naming projects:
    - Root folder should be the formal name of the project
    - Child folder must represent versioning with format v.0.0.0.0, 
      wherein the format means: version.major.minor.patches.revision
    - Examples:
      - project_alpha_and_omega
        - v.1.0.0.0
        - v.1.0.0.300
        - v.1.0.1.300
    - If the author would like to include packaging, do something like so:
      - company_name/formal_project_name
      - Complete example:
        - simplifie/coldigniter/generators/v.1.0.0.0
    
  - The purpose of this is to make downloading of libraries easily from 
    repository to localhost through CLI. Examples:
    - Searching for folders with similar keywords:
      - php index.php l list library_name
    - Fetch library_name version. Examples: 
        - php index.php l fetch project_alpha_and_omega v.1.0.0.0 //Files will be placed in libraries/paypal/v.1.0.0.0
        - php index.php l fetch project_alpha_and_omega v.2.3.4.5 //Files will be placed in libraries/paypal/v.2.3.4.5
    - Remove specific library version
        - php index.php l remove project_alpha_and_omega v.1.0.0.0 //Files in libraries/paypal/v.1.0.0.0 will be deleted
- More command lines (to be implemented) 
  - Downloadable free JS plug-ins
    - php index.php jslib list plug_in_name //Searches for folders with similar keywords.
    - php index.php jslib fetch plug_in_name version
    - php index.php jslib remove plug_in_name version
    - See public/libs for 3rd-party libraries
      - DataTables
      - Select2
      - Font Awesome
      - LightBox
      - LiquidImage
      - Slick
      - Masonry
      - DateTimePicker

- Multi-threading support

- There will be no support for ORM
