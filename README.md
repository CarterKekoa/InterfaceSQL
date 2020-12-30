# InterfaceSQL
A text based interface written in Java is used to interacts with SQL database. 
A PHP interface is also made to interact with the database using barney.

Technical Work: Part 1. Use the database you created in HW-6 (based on the CIA World Factbook) to implement the following program. Note that you can use whatever language you would like (e.g., Python, Java, C++) for the assignment. The program you write should act as a simple text-based interface over your database as described below. Note that your program can assume valid values are given except where noted below (the focus here is on practicing using SQL within a programming language, not on your ability to write a text-based UI).

1. After starting your program, it should display the following main menu.
        1. List countries       
        2. Add country      
        3. Find countries based on gdp and inflation      
        4. Update country’s gdp and inflation     
        5. Exit     
        Enter your choice (1-5):    
        
2. If a user selects 1 from the main menu, your program should display the names and codes of all of the countries. Each country should be displayed on a single line as “name (code)”, e.g., United States (US). After listing all of the countries, your program should reprompt the main menu.

3. If a user selects 2 from the main menu, your program should prompt for the country infor- mation to add to the database.
        Country code................: US        
        Country name................: United States       
        Country per capita gdp (USD): 57466       
        Country inflation (pct).....: 2.1       
        
Once given, your program should (a) check to make sure the same country code does not already exist, and if not, (b) add the corresponding country to the databse, and otherwise, (c) notify the user that the country alread exists. Once completed, your program should reprompt the main menu.

4. If a user selects 3 from the main menu, your program should prompt for the following infor- mation.
        Number of countries to display: 5       
        Minimum per capita gdp (USD)..: 10000       
        Maximum inflation (pct).......: 5       
 
Once given, your program should then display all countries with a gdp equal to or higher than the value given and an inflation equal to or lower than the inflation given. The countries should be displayed from highest-to-lowest gdp such that if two countries have the same gdp, they should be displayed from lowest-to-highest inflation. Additionally, only the number of countries entered should be displayed. For example, using the example above, if ten countries satisfy the conditions given, then only the first five are displayed, and if only three countries satisfy the above conditions, then only the three are shown. Each country should be displayed on a single line as “name (code), gdp, inflation”, e.g., United States (US), 57466, 2.1. Note that your program should not perform any sorting and should not reduce the size of the result set (i.e., you should use ORDER BY and LIMIT in your prepared statement). After the corresponding countries are displayed, your program should reprompt the main menu.

5. If a user selects 4 from the main menu, your program should prompt for the country code, new gdp, and new inflation.
Country code................: US          
Country per capita gdp (USD): 57466     
Country inflation (pct).....: 2.1       
        
Once given, your program should (a) check to make sure the country code already exists, and if so, (b) update the corresponding gdp and inflation, and otherwise, (c) notify the user that the country does not exist. Once completed, your program should reprompt the main menu.

6. If a user selects 5, your program should halt.
Technical Work: Part 2. Use HTML and PHP to implement the following. You can use the
barney server barney.gonzaga.edu to run and test your code below (like in class).

7. Write a basic HTML page that allows the user to select (using a drop-down box) a country from your HW-6 database and provides a button that when clicked displays information about the country (see below) on a separate HTML page. Name this HTML page (which includes PHP code) hw9input.php and place it in your your public html directory on barney. Note that this page must automatically populate the drop-down box with the countries in your database (i.e., you must dynamically create this drop down as opposed to just hard-coding the values as we did in class). Also, your page should provide the country id when a user presses the submit button.

8. Create a basic HTML page hw9output.php that takes the information entered on hw9input.php (via a POST request) and outputs the name, gdp, inflation, and number of provinces in each country. Your page should also display information about each city in the country as an HTML table, listing the name of the city, the province the city is located in, and the population.
