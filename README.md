# WorkshopTwo_NeighborhoodLibrary
## Requirements
- Create a Book class with:
  - Getters
  - Setters
  - Constructor
  - Methods
    - checkOut(name)
    - checkIn()
  - Properties 
    - int id
    - String isbn
    - String title
    - boolean isCheckedOut
    - String checkedOutTo
 - Create an array to hold at least 5 books
 
#### Check Out Process:
- Set checkedOutTo variable to name provided.
- Set isCheckedOut to true.

#### Check In Process:
- Set checkedOutTo variable to "".
- Set isCheckedOut to false.

### Screens
#### The Store Home Screen
- Show available books
- Show checked out books
- Exit

#### Show Available Books
- Select book to check out.
  - Prompt user for name.
  - Mark book as checked out.
- Exit to home screen.

#### Show Checked Out Books
- Check In a book (C)
  - Prompt user to enter ID to check in book
- Exit to home screen (X)

## Pseudocode
First, create a separate Book class with appropriate getters, setters and custom methods.
```
class Book {
    private int id;
    private String isbn;
    private String title;
    private boolean isCheckedOut;
    private String checkedOutTo;
    public Book(int id, String isbn, String title, boolean isCheckedOut, String checkedOuTo) {
        this.id = id;
        this.isbn = isbn;
        this.title = title;
        this.isCheckedOut = isCheckedOut;
        this.checkedOutTo = checkedOuTo;
    }

    public int getId() {
        return id;
    }
    public String getIsbn() {
        return isbn;
    }
    public String getTitle() {
        return title;
    }
    public boolean isCheckedOut() {
        return isCheckedOut;
    }
    public String getCheckedOutTo() {
        return checkedOutTo;
    }

    public void setId(int id) {
        this.id = id;
    }
    public void setIsbn(String isbn) {
        this.isbn = isbn;
    }
    public void setTitle(String title) {
        this.title = title;
    }
    public void setCheckedOut(boolean checkedOut) {
        isCheckedOut = checkedOut;
    }
    public void setCheckedOutTo(String checkedOutTo) {
        this.checkedOutTo = checkedOutTo;
    }
```
Create an array to hold at least 5 books.
```
Book[] bookArr = new Book[5];
bookArr[0] = new Book(423986251, "0385474547", "Things_Fall_Apart", false, "");
bookArr[1] = new Book(425855903, "070993007508", "The_Notebook", false, "");
bookArr[2] = new Book(436777437, "1531831281", "Hunger_Games", false, "");
bookArr[3] = new Book(428079958, "9780062024039", "Divergent", false, "");
bookArr[4] = new Book(448556923, "014242417X", "The_Fault_In_Our_Stars", false, "");
```
Create method to check out books.
```
    public void checkOut(String name){
        this.checkedOutTo = name;
        this.isCheckedOut = true;
    }
```

Create method to check in books.
```
    public void checkIn(){
        this.checkedOutTo = "";
        this.isCheckedOut = true;
    }
```
