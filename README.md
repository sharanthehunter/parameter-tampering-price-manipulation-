# parameter-tampering-price-manipulation-

I have found that you can buy any products in less amount or even we can say as free by changing the price of the product!!

Target:

![image](https://user-images.githubusercontent.com/84071887/204717084-a8d01e4e-856e-45d0-bef9-1208d61bccb3.png)

Vulnerability name: Parameter Tampering

Steps To Reproduce:

1. Go to this website https://www.mytheresa.com/
2. Create an account or login using your details
3. Add items to the cart and click proceed to check out

![image](https://user-images.githubusercontent.com/84071887/204717764-32773502-2be7-47fc-8066-ee1133c95e22.png)

4. Enter your delivery details and go to the next step

![image](https://user-images.githubusercontent.com/84071887/204717968-4138aff8-0421-4f9e-abb0-56c544cb3ee2.png)

5. Select your payment method
6. I am selectiing PayPal method
7. Before clicking complete purchase intercept the request in the burp suite
8. change the amount to your wish 

![image](https://user-images.githubusercontent.com/84071887/204718394-45d73232-535a-4b62-a222-ce7517cee0a7.png)



Request:
,"amount":415,"currencyIsoCode":"EUR",


9. After changing the price forward the request
10. you will get the PayPal page to pay the change amount.

![image](https://user-images.githubusercontent.com/84071887/204718562-0ff4fc97-7506-4e89-97ee-3cc9ddeb9afd.png)


BOOM!!!!!  The price was changed, pay and get the product.


I have attached POC Video, Please take a look!!


Impact:
The attacker can reduce the price of the order and make a financial loss!!  
