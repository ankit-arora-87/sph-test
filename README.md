Your customer "Jugaad Patches Pvt Ltd" wants to build their portal with Drupal 9. They sell their products only on their mobile app. (Yeah, that's not a great thing to do, but you know.) This website has just a listing of their products. 

Each product page shows 
1. The product title
1. An Image
1. Product Description
1. App Purchase Link (Just a simple http link, don't let the word app confuse you.)

Instead of displaying the 'App Purchase Link' on the site on the product page, Jugaad Patches would like to display the link as a QR code, such that the site visitors can quickly open the product on the Jugaad app on their mobile. 

Here is where You, the Drupal expert, was flown in to build this stuff. 

Should you choose to accept this mission, you shall build the following:
1) A Drupal content type to hold all their products
2) A Drupal block that can be placed on any product page

The block, when placed on any product page, automatically shows the currently displayed product's App Purchase Link as a QR code, that the site visitors can scan using their mobile. 

![](https://user-images.githubusercontent.com/3456349/37258010-328dd226-2597-11e8-9534-2e0d1e7d0d40.png)

**While you are almost good to get started now, make sure to stick to the below guidelines:**
1. Don't use any contrib modules. While there are a ton of contrib modules out there that can help accomplish this, and although it is usually a good practice to use contrib modules over custom code, this exercise is aimed at checking how well you can code. So, stick to building a custom module. 
2. You are free to use any publicly available PHP (or otherwise) libraries to generate the QR code. You don't have to reinvent the wheel! Use something from https://packagist.org/?q=php%20qrcode&p=0
3. Your code submission is expected to be minimal. Just a custom module, which when copied in a Drupal 9 website's modules folder, and after a "composer install", followed by enabling the module, will make the required content type and block available. (Bonus points if enabling the module also places the block in, say, the right sidebar). **Do not use a HTTP API like Google Charts API** to generate the QR code. Use any library available in packagist.org only. 

4. You are not absolutely required to provide a layout to the product page. But good if you can do it. Although, stick to our rule of 'no contrib modules'. 
5. Don't worry about creating dummy content, including the product shown in the wireframes, as part of your module. You are good as long as the content type and the blocks are functional in the module checked in.
6. If your submission requires any further deployment steps, apart from the ones already listed in #3 above, make sure to list such deployment/installation steps. (Don't do it with an email. Instead, update this README.md file with the instructions). 
7. Don't worry about the homepage. You can build a basic listing of products on the homepage for some bonus points, but that's not really required for this exercise. 
8. Make the module available, along with the sample content (Unicorn Iron on patch), on a publicly available url. You may use Acquia Cloud Free Tier hosting available at https://insight.acquia.com/free/register?cs=acf-expertdevs , to upload your demo site. 
9. Your final submission is expected to contain a) Updated code of the module in this repository b) A link to the demo site c) Admin (uid=1) credentials to the demo site 

Wish you the very best!

------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------------------

**Submission Details:**
 1. Updated code of the module in this repository: 
    - Pushed newly created custom module named as "jugaad_patches_product"
    - Prerequisite before enabling our custom module
        - Need to install QR code dependency: 
            composer require endroid/qr-code
    - After enabling/ installing our custom module (jugaad_patches_product) will create custom content type named as "Jugaad Patches Store - Product" with required listed fields in the above requirement section
    - It will also create QR code block & put it into right sidebar section which you can see for node detail page (after adding content for our custom content type: Jugaad Patches Store - Product)
    - It also contains a basic view to list out all the added products (/products). Currently site home page also routed to this products page.
 2. A link to the demo site: 
    - Home: https://dev-jugaad-patches-store.pantheonsite.io
    - Product Detail: https://dev-jugaad-patches-store.pantheonsite.io/unicorn-iron-on-patch
 3. Admin (uid=1) credentials to the demo site:
    - Admin Login: https://dev-jugaad-patches-store.pantheonsite.io/user/login
    - Username: admin
    - Password: KXMJZp2es2qcJX9
