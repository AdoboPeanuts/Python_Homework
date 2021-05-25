# PyRamen

## Key Objectives:
```
1. Import menu_data.csv file and sales_data.csv file.

2. Read in menu_data.csv

	Initialize an empty menu list object to hold the contents of menu_data.csv.


	Use a with statement and open the menu_data.csv by using its file path.


	Use the reader function from the csv library to begin reading menu_data.csv.


	Use the next function to skip the header (first row of the CSV).


	Loop over the rest of the rows and append every row to the menu list object (the outcome will be a list of lists).


3. Set up the same process to read in sales_data.csv. Append every row of the sales data to a new sales list object.

4. Manipulate Date

	Complete the following:


	Initialize an empty report dictionary to hold the future aggregated per-product results. The report dictionary will eventually contain the following metrics:


	01-count: the total quantity for each ramen type


	02-revenue: the total revenue for each ramen type


	03-cogs: the total cost of goods sold for each ramen type


	04-profit: the total profit for each ramen type


Loop through every row in the sales list object.


For each row of the sales data, set the following columns of the sales data to their own variables:

	Quantity

	Menu_Item



Perform a quick check if the sales_item is already included in the report. If not, initialize the key-value pairs for the particular sales_item in the report. Then, set the sales_item as a new key to the report dictionary and the values as a nested dictionary containing the following:
{
"01-count": 0,
"02-revenue": 0,
"03-cogs": 0,
"04-profit": 0,
}




Create a nested loop by looping through every record in menu.


For each row of the menu data, set the following columns of the menu data to their own variables:

Item

Price

Cost


If the sales_item in sales is equal to the item in menu, capture the quantity from the sales data and the price and cost from the menu data to calculate the profit for each item.

Cumulatively add the values to the corresponding metrics in the report like so:
report[sales_item]["01-count"] += quantity
report[sales_item]["02-revenue"] += price * quantity
report[sales_item]["03-cogs"] += cost * quantity
report[sales_item]["04-profit"] += profit * quantity

Else print the message "{sales_item} does not equal {item}! NO MATCH!".

5. Write out the contents of the report dictionary to a text file. The report should output each ramen type as the keys and 01-count, 02-revenue, 03-cogs, and 04-profit metrics as the values for every ramen type as shown:

Resulting manipulation should look similar to the following:

spicy miso ramen {'01-count': 9238, '02-revenue': 110856.0, '03-cogs': 46190.0, '04-profit': 64666.0}
tori paitan ramen {'01-count': 9156, '02-revenue': 119028.0, '03-cogs': 54936.0, '04-profit': 64092.0}
truffle butter ramen {'01-count': 8982, '02-revenue': 125748.0, '03-cogs': 62874.0, '04-profit': 62874.0}
tonkotsu ramen {'01-count': 9288, '02-revenue': 120744.0, '03-cogs': 55728.0, '04-profit': 65016.0}
vegetarian spicy miso {'01-count': 9216, '02-revenue': 110592.0, '03-cogs': 46080.0, '04-profit': 64512.0}
shio ramen {'01-count': 9180, '02-revenue': 100980.0, '03-cogs': 45900.0, '04-profit': 55080.0}
miso crab ramen {'01-count': 8890, '02-revenue': 106680.0, '03-cogs': 53340.0, '04-profit': 53340.0}
nagomi shoyu {'01-count': 9132, '02-revenue': 100452.0, '03-cogs': 45660.0, '04-profit': 54792.0}
soft-shell miso crab ramen {'01-count': 9130, '02-revenue': 127820.0, '03-cogs': 63910.0, '04-profit': 63910.0}
burnt garlic tonkotsu ramen {'01-count': 9070, '02-revenue': 126980.0, '03-cogs': 54420.0, '04-profit': 72560.0}
vegetarian curry + king trumpet mushroom ramen {'01-count': 8824, '02-revenue': 114712.0, '03-cogs': 61768.0, '04-profit': 52944.0}


3. Export main.ipynb to PyRamen folder.

```