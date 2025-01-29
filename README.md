# Library-project-python-

# functions used
class

_init_

def

# Selecting keys :
1.display available books

2.display all books

3.borrow a book

4.return a book

5.quit


# Developed coad :
        user_choice =int(inp

class library():
    def __init__(self,list):
        self.books_list=list
        self.available_books_list= list[:]
        self.books_lent={}  ###key-book value-user name
    def display_available_books(self):
        for book in self.available_books_list:
            print(book)
    def display_all_books(self):
        for book in self.books_list:
            print(book)
    def lend_book(self,name,book):
        if book not in self.books_list:
            print("incorrect book name .please check book list")
            return
        if book in self.available_books_list:
            self.books_lent.update({book:name})
            self.available_books_list.remove(book)
            print("you can take the book..")
        else:
            print("the book is already taken by " + self.books_lent[book])
    def return_book(self,):
        del self.books_lent[book]
        self.available_books_list.append(book)
if __name__=="__main__":
    lib = library(["the life divine","da vinci code","the alchemist","education","comics"])
    print("welcome to library.enter an option.")
    while True :
        print("1.display available books")
        print("2.display all books")
        print("3.borrow a book")
        print("4.return a book")
        print("5.quit")
        user_choice =int(input())
        if user_choice==1:
            lib.display_available_books()
        elif user_choice==2:
            lib.display_all_books()
        elif user_choice==3:
            name =input("enter user name")
            book =input("enter book name")
            lib.lend_book(name,book)
        elif user_choice==4:
            book =input("enter the name of the book")
            lib.return_book()
        elif user_choice==5:
            break
        else:
            print("invalid choice")
