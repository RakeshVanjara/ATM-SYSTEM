class Bank:
    balance = 5000 #balance can be dynamic

    def login(self, pin):
        if pin == 1111: #pin can be taken dynamically and also saved dynamically
            return True
        else:
            return False

    def credit(self, amt):
        self.balance += amt

    def debit(self, amt):
        self.balance -= amt

    def display(self):
        print("Current balance is " + str(self.balance))


obj = Bank()
flag = False
for i in range(1, 4):
    if obj.login(int(input("enter pin code:- "))):
        flag = True
        break
if flag:
    while True:
        o = input("""
             Press 1 for Deposit
             Press 2 for Withdraw
             Press 3 for Acc Balance
             Press 4 for exit
             ---------------------   >""")
        if o == '1':
            obj.credit(int(input("enter amount for credit:- ")))
            print("After credit total amount is, ")
            obj.display()
        elif o == '2':
            amt = int(input("enter amount for debit:- "))
            if amt < obj.balance:
                obj.debit(amt)
                print("After debit total amount is, ")
            else:
                print("insufficient balance:- ")
            obj.display()
        elif o == '3':
            print("Total balance is :- ")
            obj.display()
        elif o == '4':
            exit(0)
else:
    print("Your pin code attempt has been completed")
