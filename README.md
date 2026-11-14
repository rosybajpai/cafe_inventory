# Campus Cafe Inventory

This is a small Java program for keeping track of products in a campus cafe. From the menu, you can add products, see what’s in stock, check the total stock value and average price, restock an item, or make a copy of one.

## Running the program

Open the project in IntelliJ IDEA and run `Main`. To see the warm-up example, run `Warmup` separately.

## Warm-up

I thought the first line would be `7 5.0 130`, and that the switch would print `One`, `Two`, and `Three`. It actually printed `7 5.0 -126`, then `Two` and `Three`: converting 130 to a `byte` gives -126, and the switch starts at case 2 and continues to case 3 because there are no `break` statements.

## What I learned

### Static and instance variables

`totalProducts` is shared by every `Product` object, so it keeps one count for the whole class. Fields like `name` belong to individual objects, which means each product can have a different name.

### Copy constructor

The copy constructor makes a new product using the name, price, and quantity of an existing one. The new product is separate, so changing the copy’s name doesn’t change the original’s name.

### Casting

Java makes me write an explicit cast when I convert a `double` to an `int` because the decimal part could be lost. The cast drops that part instead of rounding, so '25.25' becomes '25'.

## Test session

The full console session, including an invalid input, is saved in `output.txt`.