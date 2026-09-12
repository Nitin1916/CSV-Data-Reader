# CSV-Data-Reader
Importing CSV ,using .DictReader ,setting up variable and reading each row and updating variables 

import CSV
total_sales=0
count=0
highest_sale=0
highest_product=""
filename=input("Enter the filename,:")
with open("filename","r") as file:
   reader=csv.DictReader(file)
   try:
      for row in reader:
      product=row["product"]
      sale=float(row["sales"])
      total_sales+=sale
      count+=1
      if sale>highest_sales:
         highest_sale=sale
         highest_product=product
   except:
      print("Invalid data slipping")

avg_sales=total_sales/count

print("//Sales Report//")
print("avg_sales::",avg_sales)
print("highest sale::",highest_sales)
