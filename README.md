# Test
This
class Student:
    def __init__(self, name, roll_no, m1, m2, m3):
        self.name = name
        self.roll_no = roll_no
        self.marks = [m1, m2, m3]

    def total_marks(self):
        return sum(self.marks)

    def percentage(self):
        return self.total_marks() / 3

    def display(self):
        print("Name:", self.name)
        print("Roll Number:", self.roll_no)
        print("Marks:", self.marks)
        print("Total Marks:", self.total_marks())
        print("Percentage:", self.percentage())


# Example usage
s1 = Student("Rahul", 101, 80, 75, 90)
s1.display()










class BankAccount:
    def __init__(self, acc_no, holder_name, balance=0):
        self.acc_no = acc_no
        self.holder_name = holder_name
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount
        print("Deposited:", amount)

    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            print("Withdrawn:", amount)
        else:
            print("Insufficient Balance!")

    def display(self):
        print("Account Number:", self.acc_no)
        print("Account Holder:", self.holder_name)
        print("Balance:", self.balance)


# Example usage
acc = BankAccount(12345, "Amit", 5000)
acc.display()
acc.deposit(2000)
acc.withdraw(3000)
acc.display()













class Book:
    def __init__(self, book_id, title):
        self.book_id = book_id
        self.title = title
        self.status = "Available"

    def issue(self):
        if self.status == "Available":
            self.status = "Issued"
            print("Book Issued Successfully.")
        else:
            print("Book already issued.")

    def return_book(self):
        self.status = "Available"
        print("Book Returned Successfully.")

    def display(self):
        print("Book ID:", self.book_id)
        print("Title:", self.title)
        print("Status:", self.status)


# Example usage
b1 = Book(1, "Python Programming")
b1.display()
b1.issue()
b1.display()
b1.return_book()
b1.display()
