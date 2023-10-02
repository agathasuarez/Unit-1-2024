# Crypto Wallet

![](22ROOSE-master768.gif)  
<sub>Illustration for Glenn Harvey</sub>

# Criteria A: Planning

## Problem definition

Ms. Sato is a local trader who is interested in the emerging market of cryptocurrencies. She has started to buy and sell electronic currencies, however at the moment she is tracking all his transaction using a ledger in a spreadsheet which is starting to become burdensome and too disorganized. It is also difficult for Ms Sato to find past transactions or important statistics about the currency. Ms Sato is in need of a digital ledger that helps her track the amount of the cryptocurrency, the transactions, along with useful statistics. 

Apart for this requirements, Ms Sato is open to explore a cryptocurrency selected by the developer.
| Name   | Coin            |   | Name | Coin |
|--------|-----------------|---|------|------|
| Keeler | ETH             |   |      |      |
| Rocky  | DOGE            |   |      |      |
| Yuiko  | BNB(Binance)    |   |      |      |
| Jan    | Tether (USDT)   |   |      |      |
| Antoni | XRP(Ripple)     |   |      |      |
| Victor | Cardano (ADA)   |   |      |      |
| Manaha | LTC (LIte Coin) |   |      |      |
| Marina | Solano (SOL)    |   |      |      |
| May    | (DAI)           |   |      |      |
| Ayane  | Zcash (ZEC)     |   |      |      |
| Yosuke  | USD COIN  (USDC)  |   |      |      |
| Naomi  |  TRX Tron       |   |      |      |
| Amine  |  KLIMA          |   |      |      |
| Dylan  | Monero XMR      |   |      |      |
| Agatha | Shiba Inu (SHIB)|   |      |      |


An example of the data stored is 

| Date | Description | Category | Amount  |
|------|-------------|----------|---------|
| Sep 23 2022 | bought a house | Expenses | 10 BTC |
| Sep 24 2022 | food for house celebration | Food | 0.000001 BTC |


## Proposed Solution

Design statement:
I will to design and make a easy to use electronic ledger for a client who is an ordinary person, so the wallet will use as simple vocabulary as possible, attractive design and perform main functions. To meet all these requirements python will be used as the programming language. It will take 30 hours to make and will be evaluated according to the criteria "Design" and "Development" .

Shiba Inu is coin for this project. This cryptocurrency was created in August 2020 by an anonymous person.  Shiba-inu is a Japanese breed of dog, and this name was used for the name of the currency. 1 SHIB = 0.0000074 USD


## Success Criteria
1. The electronic ledger is a text-based software (Runs in the Terminal).
2. The electronic ledger display the basic description of the cyrptocurrency selected.
3. The electronic ledger allows to enter, withdraw and record transactions.
4. The electronic ledger allowed to create new data for entry
5. The electronic ledger showed every amount in 4 currencies
6. The electronic ledger has design and construction which are developed for maximum ease of use

# Criteria B: Design

## System Diagram
![Image alt](https://github.com/{username}/{repository}/raw/{branch}/{path}/image.png)

## Flow Diagrams


## Record of Tasks


| Task No  | Planned Action | Time estimate | date |  criterion  |
|------|-------------|----------|---------| --------|
| 1       | Create available options| 40min  | Sep 18  | b   | 
|2| Think about program and write Success Criteria| 30min|Sep 18|a| 
|3| Create desine for main menu|30min| Sep 18|c|
| 4       | Create main functions for use throughout the program (go menu, error, goodbye)| 90min         | Sep 20 | c|    
|5 Add all available colors for  for program design|20 min| Sep 21|b| 
| 6       | Create function "exchanging" for option 2 | 90min | Sep 21 | c|             
| 7       | Create option "view account" | 10min  | Sep 22 | c|             
| 8       | Create options "top up account" and "Funds transfer"  |  80min         | Sep 23 |c|        
| 9       | Create option "Transaction history" | 40min         | Sep 26  |c|            
| 10       | Create option "TAdd a new account" | 30min         | Sep 27|c|
| 11       | Add colors    |   20min         | Sep 28   |b|           

# Criteria C: Development

## Login System
Part of the code that is responsible for opening the program using the correct login and password. All correct logins and passwords are saved in users.csv

    def try_login(name: str, password: str) -> bool:
    
    with open('users.csv', mode='r') as f:
    
        data = f.readlines()
        
    for line in data:
    
        parts = line.strip().split(',')
        
        if len(parts) == 2:
        
            uname, upass = parts
            
            if uname == name and upass == password:
            
                return True

    return False

# Testing

1). All colors for using during the code

    blue ="\33[1;94m"
    
    green = "\33[1;92m"
    
    red = "\33[1;91m"
    
    yellow = "\33[1;93m"
    
    cyan = "\33[1;96m"
    
    white ="\33[1;97m"
    
    purple = "\33[1;95m"

2). Function ERROR which will be used if user enter data with a mistake 

    def error():
        print(f"{red}ERROR{red}\nThe option is missing, try again")
        menu()


3). Function GO TO MENU which will be used after every step. User is able to retern to menu without entering login/password every time
    def go_m():
        m = input("Do you want to go to the main menu? Yes/No: ").lower()
        if m == "yes":
            menu()
        elif m == "no":
            print ("You are logged out")
            end_code = "\033[00m"
            color = "\33[1;91m"
            print (f"{color}Goodbye{end_code}")
        else:
            error()





```
