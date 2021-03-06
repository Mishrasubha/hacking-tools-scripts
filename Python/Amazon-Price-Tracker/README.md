## Amazon Price Tracker 
- This script built in Python is an Amazon Price Tracker. 
- The user enters :
    - The URL of the product of which he would like the track the price of.
    - His/Her budget for the product.
    - His/Her Email credentials.
- The script runs continuously and checks on the price of the product every 12 hours.
- If the price of the product is equal to or below the user's budget, the user receives an email confirmation.
- The price of the product is logged into a file named price_logger.txt every 12 hours.

## Working 
- The BeautifulSoup library is used to scrape the price of the product from the Amazon site.
- On Amazon, the prices of products are either expressed as a range or as a single number.

![Image](assets/single.png)


![Image](assets/range.png)

- If the budget is within the range, an email will be sent.
- In the script, headers need to be used to make the get request to the Amazon site.
- In place of headers, the user must replace it with the result of **my user agent** must be used instead.

![Image](assets/myagent.png)

- The Email settings of the user must be configured to operate on less secure mode to facilitate the sending of emails.

![Image](assets/lesssecure.png)

- After this, the script can be run.

![Image](assets/mail.png)

![Image](assets/email.png)

- Using this as an example

![Image](assets/single.png)

- The user enters 700 rupees as the budget, as the price is lesser than the budget the following email is sent, else the program continues to run till the condition is satisfied.

![Image](assets/confirm.png)

- The prices are also logged into the file price_logger.txt as shown, so the user will have an account of the changes the price underwent.

![Image](assets/change.png)

![Image](assets/change.png)

## Usage
- Requirements
  - Requests 
  - BeautifulSoup
  - smptplib
 
 - The user is prompted to enter the URL of the price of the product that needs to be tracked
 - The user is also prompted to enter the budget
 - The email credentials of the user are asked as an email is sent when the price of the product is within the budget
 - For this the email settings must be set to less secure mode
 - The changes observed in the price of the product are also logged for reference
