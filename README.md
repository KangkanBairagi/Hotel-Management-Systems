# Hotel-Management-Systems

Code:


class hotel:

    def __init__(self, rt='', s=0, p=0, r=0, t=0, a=150, name='', address='', cindate='', coutdate='', rno=1):

        print("\n\n === Hotel Management Systems ===\n")
        #self.rno = rno
        self.rt = rt

        self.r = r

        self.t = t

        self.p = p

        self.s = s
        self.a = a
        self.name = name
        self.address = address
        self.cindate = cindate
        self.coutdate = coutdate
        self.rno = rno

    def inputdata(self):
        self.name = input("\nEnter your Fullname: ")
        self.address = input("\nEnter your address: ")
        self.cindate = input("\nEnter your check in date: ")
        self.coutdate = input("\nEnter your checkout date: ")
        print("Your room no.: ", self.rno, "\n")

    def showdata(self):
        print("******SHOW CUSTOMER DETAILS******")

        print("Customer name:", self.name)
        print("Customer address:", self.address)
        print("Check in date:", self.cindate)
        print("Check out date", self.coutdate, "\n")

    def roomrent(self):

        print("We have the following rooms for you:-")

        print("1.  Class A----> 4000")

        print("2.  Class B----> 3000")

        print("3.  Class C----> 2000")

        print("4.  Class D----> 1000")

        x = int(input("Enter the number of your choice Please-: "))

        n = int(input("For How Many Nights Did You Stay: "))

        if (x == 1):

            print("you have choose a room Class A")

            self.s = 4000 * n

        elif (x == 2):

            print("you have choose a room Class B")

            self.s = 3000 * n

        elif (x == 3):

            print("you have choose a room Class C")

            self.s = 2000 * n

        elif (x == 4):
            print("you have choose a room Class D")

            self.s = 1000 * n

        else:

            print("please choose a room")

        print("your choose room rent is =", self.s, "\n")

    def foodpurchased(self):

        print("*****Food MENU*****")

        print("1.Dessert-----> 100")
        print("2.Drinks-----> 50")
        print("3.Breakfast----> 90")
        print("4.Lunch----> 110")
        print("5.Dinner----> 150")
        print("6.Exit")

        while (1):

            c = int(input("Enter the number of your choice:"))

            if (c == 1):
                d = int(input("Enter the quantity:"))
                self.r = self.r + 100 * d

            elif (c == 2):
                d = int(input("Enter the quantity:"))
                self.r = self.r + 50 * d

            elif (c == 3):
                d = int(input("Enter the quantity:"))
                self.r = self.r + 90 * d

            elif (c == 4):
                d = int(input("Enter the quantity:"))
                self.r = self.r + 110 * d

            elif (c == 5):
                d = int(input("Enter the quantity:"))
                self.r = self.r + 150 * d

            elif (c == 6):
                break;
            else:
                print("You've Enter an Invalid Key")

        print("Total food Cost=Rs", self.r, "\n")

    def display(self):
        print("******HOTEL BILL******")
        print("Customer details:")
        print("Customer name:", self.name)
        print("Customer address:", self.address)
        print("Check in date:", self.cindate)
        print("Check out date", self.coutdate)
        print("Room no.", self.rno)
        print("Your Room rent is:", self.s)
        print("Your Food bill is:", self.r)

        self.rt = self.s + self.t + self.p + self.r

        print("Your sub total Purchased is:", self.rt)
        print("Additional Service Charges is", self.a)
        print("Your grand total Purchased is:", self.rt + self.a, "\n")
        self.rno += 1


def main():
    a = hotel()

    while (1):
        print("1.Enter Customer Information: ")

        print("2. Show Customer Details: ")

        print("3.Calculate Room Rent: ")

        print("4.Calculate Food Purchased: ")

        print("5.Show Total Cost: ")

        print("6.EXIT")

        b = int(input("\nEnter the number of your choice: "))
        if (b == 1):
            a.inputdata()

        if (b ==2):
            a.showdata()

        if (b == 3):
            a.roomrent()

        if (b == 4):
            a.foodpurchased()

        if (b == 5):
            a.display()

        if (b == 6):
            quit()


main()
