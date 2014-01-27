Zaakpay Module for Magento
==========================

Instructions:
=============

[] Fill up Zaakpay integration form
  - Login to your Zaakpay Account and Go to My Account > Integration
  - For Transact API Return Url, enter the following url
    <http://youtstorehomeurl.com>/zaakpay/transact/response
  - Enter other details, generate key and press save

[] Adding module files to your magento installation
  - Please take a backup of your code for safety.
  - Merge the contents of the app directory with the app directory of your magento installation.
  - Merge the contents of the lib directory with the lib directory of your magento installation. 

[] Enabling the module and configuring it with your zaakpay merchant credentials
  - Login to your magento admin and go to System > Configuration.
  - On the left side bar, scroll down and click on "Advanced" under the Advanced section.
  - Scroll down the page and "Enable" the Zaakpay module.
  - On the same page, click on "Payment Methods" on the sidebar under the section "SALES".
  - On this page, a "Zaakpay Webpay checkout" section will appear. Click on it if its not already open.
  - Add your Merchant Id, secret key here. Also specify whether sandbox mode (test mode) will be enabled or disabled. 
    click "Save Config".
    Additionally, if you want that only buyers from particular country or countries should be able to use zaakpay,  
    against the "Payment Applicable From" field, select "Specific Countries" and then select the countries in the box
    that opens up. In order to select more than one country, you will need to click on the countries with ctrl key of the 
    keyboard pressed. Sort Order field determines in which order zaakpay will be displayed to the buyer during checkout.
   
[] Testing Zaakpay 
  - Make sure that sandbox mode is on and all details are entered in the zaakpay configuration
  - Go to your store and place and order. 
  - If you configured zaakpay correctly in the previous step, it should appear as an option under payment methods
    during checkout
  - When you click on checkout, it should redirect you to Zaakapay's site and show credit card form. 
  - Use a test card from below to complete a fake payment 
  
[] Test Cards
   Type        CARD NO               CVV     EXPIRY      Name    Month
   VISA        4012888888881881      123      2015       TEST     12
   VISA        4123450131001381      879      2015       TEST     12
   Master      5177194127672001      548      2015       TEST     12
   Master      5453010000064154      896      2015       TEST     12
  
[] Checking the status of payment transaction at Zaakpay's end from your magento admin
  - Login to admin and under Sales, click on Orders
  - Click on the first order in the data grid. This should be the order that you just placed
  - When the order details page opens up, look for "Payment Information" block. 
    Inside the block, you can see the latest status of the transaction on zaakpay's end. 

[] Asking Zaakpay to capture payment remotely from the magento admin
  - To send a call to capture funds, create an invoice by clicking the button "invoice" among the top-right buttons 
    Scroll down and look for the block "Invoice Total". 
    Against the "Amount" field, select capture online and click on submit invoice.     

[] Asking Zaakpay to cancel transaction remotely from the magento admin
  - To update the status of the zaakpay transaction to cancelled, click on either cancel or void button..
