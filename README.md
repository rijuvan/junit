# junit

Topic: JUnit  Lab Part 1


1.	Write test cases for  for Loan Sanction which checks the eligibility of an applicant .
Create a class  LoanCalculator with getLoanEligibilty(), which reads take home salary ,experience and all other inputs and  returns  eligibility on the basis of below given table .

Experience	Monthly take home	Eligible amount
0-5	0-20000	0
5 -10	20001-60000	monthly take home *15
above 10	above 60 K	monthly take home *20


2.	Create a class CreditCardOperation . Credit cards usually have a so-called check digit. This is a single digit that that is  assigned when the account number is developed and has a special property. One particularly simple mechanism is to assign the last digit of the sum of all the other digits. 
For example, suppose we have a nine-digit account number (including the check digit). The check digit would be the sum of the eight digits. This digit could be placed any where  in the sequence, say the third digit. As a full example, suppose the eight numbers are 12345678. Their sum is 36; thus  6 is the check digit. The account number is therefore 126345678. Write"valid" or "invalid" for the results of the test.Create test cases for above application  . Write tests for sanity .

Topic :  Unit Testing : Parametrized Test  ,Theory,Rule,Exception Handling
3 . Create a class  Stock that holds information about stocks. Stock class  attributes are :
private String tickerSymbol;
private String name;
A class  named StockList that uses the Stock Objects and provides business methods to test  that enables it to maintain the Stock Objects.
Methods of StockList class are:
public String getStock(String ticker);
public void addStock(String ticker, String name);
public void updateStock(String ticker, String name);
public void deleteStock(String ticker);
Write a seprate  class StockOperationTest contains test
Test1: to add stock
Test2: remove stock
Test3: display full stock.
Test4:  update stock 
Stock sample data:  Use appropriate annotation to initialize the stock
 ('ABC', 'ABC Company');
 ('ZZZ', 'Zigby Zebras');
 ('ICS', 'Internet Corp of Slobovia');
 ('DDC', 'Digby Door Company');
 ('ZAP', 'Zelenarinski Ltd.');
 ('JIM', 'Jimco');
 ('SRU', 'Stocks R Us');
 ('SRI', 'Shelves and Radios Inc');
 ('FBC', 'Foo Bar Company');
 ('DDBC', 'Ding Dong Bell Company');
 ('UDE', 'Upn Down Elevator Company');
 
 ---- End ----------------
 
 
 
 
 Topic :  Mockito and Junit : Junit , Mockito,Code Coverage ,BDD
1.	 Example maintains a database of all books available in the library. Books are stored in a table with the following structure: ( Data base is not available so we have to use Mockito farmeowrk to test all DB Opeations )
create table BOOKS (id int,title varchar(64), author varchar(32), publisher varchar(32),   isbn varchar(16),       pages int, category varchar(32), CONSTRAINT PK_PRODUCTS PRIMARY KEY (id));
To keep it simple we make the following assumptions:
•	the library has only one copy for each book
•	each book is written only by one author
•	each book belongs to only one category
 The BookService Calss  should allow you to:
•	create new entries in the BOOK table
•	retrieves a book by title
•	retrieve all books in a certain category
•	retrieve all books written by a certain author

Write a BookOpeationTest Class  that performs the following test using mockito . If there is a method wchich returns void then verify suing Mockito and if required also use method ordering .
•	add 3 new books to the library
•	find a book given its title and print the book information
•	retrieves all books in a given category and prints their information
•	retrieves all books written by a certain author and prints their informatio
2.	The final example consists of writing a complete  tests  for the Library example we have been using in our assignments. 
The library maintains a database with information about the following entities:
•	all books available in the library
•	users of the library
•	which book is checked out by which user
The above information is stored in database tables having the following definition: Database is not available 
Create table BOOKS (
        id int,
        title varchar(64), 
        author varchar(32), 
        publisher varchar(32),
        isbn varchar(16),
        pages int,
        category varchar(32),
        user_id int,
        CONSTRAINT PK_BOOKS PRIMARY KEY (id),
        CONSTRAINT FK_USER FOREIGN KEY (user_id) REFERENCES USERS(id)
);

create table USERS (
        id int,
        name varchar(32),
        e_mail varchar(32),
        phone varchar(15),
        address varchar(64),
        CONSTRAINT PK_USERS PRIMARY KEY (ID)
);

For simplicity, we make the following assumptions:
•	the library has only one copy for each book
•	each book is written only by one author
•	each book belongs to only one category
Implement following test for below functionalities :
•	users log into the system by providing their e-mail address and password
•	after logging in they are allowed to browse the books by author, category, or both
•	user can add books to a shopping cart (or list of books to check out)
•	users can check out the books in their cart. When books are checked out, the corresponding user_id field stores the id of the user.
•	When books are checked out an e-mail notification is sent to the user e-mail address. The content of the e-mail is a summary including the date and title, author and publisher information for each book checked out.
•	Presumably, the books will be fetched by a clerk and given or shipped to them. However we are not implementing this feature in any way.
•	Users can check in books from the complete list of books they have checked out.
•	Presumably the above operation will be performed by a clerk of the library, but we let the user do it here for simplicity and to make it easy to test our application.
Note : Assumption can be made by the developer are also accepted. Finally generate the coverage report for the application .



