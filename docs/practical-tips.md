## Practical Tips
Assume that Amy, Brian, Claire go traveling together, and they are trying to use Tour-Balance.

### Scenario 1- normal payment
- To get two same price tickets, Amy paid total $600 for Claire and herself.
    ```
    [Form]
    - Who Paid: Amy
    - Amount: 600
    - Who needs to share: Amy, Claire
    ```

### Scenario 2- payment with unequal amount
- Amy's food is $200. Brian's is $100. Claire's is $150. And Amy paid for all first.
    ```
    [1st Form]
    - Who Paid: Amy
    - Amount: 100
    - Who needs to share: Brian
    ```
    ```
    [2nd Form]
    - Who Paid: Amy
    - Amount: 150
    - Who needs to share: Claire
    ```

### Scenario 3- advance payment
- Before they go traveling, Amy and Claire gave Brian $1000 in advance individually.
    ```
    [1st Form]
    - Who Paid: Amy
    - Amount: 1000
    - Who needs to share: Brian
    ```
    ```
    [2nd Form] 
    - Who Paid: Claire
    - Amount: 1000
    - Who needs to share: Brian
    ```

### Scenario 4- final balance
1. Assume the final balance as below,
    - Amy needs to take out $1500
    - Brian needs to take out $1000
    - Claire needs to get $2500
2. Choose one as a host. Take Brian as an example.
3. People who needs to take out money should give it to the host. So Amy gives $1500 to Brian.
    ```
    [1st Form]
    - Who Paid: Amy
    - Amount: 1500
    - Who needs to share: Brian
    ```
4. Reload the final sheet, then
    - Amy needs to do nothing
    - Brian needs to take out $2500
    - Claire needs to get $2500
5. The host gives money to people who needs getting money. So Brian gives $2500 to Claire.
    ```
    [2nd Form]
    - Who Paid: Brian
    - Amount: 2500
    - Who needs to share: Claire
    ```
6. Reload the final sheet again, now all the money is already balanced.
