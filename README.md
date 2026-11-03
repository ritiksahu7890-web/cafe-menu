# A simple Cafe Management System

# 1. Define the items and their prices
menu = {
    "coffee": 80,
    "tea": 40,
    "pizza": 250,
    "burger": 120,
    "fries": 70
}

# 2. Show the welcome message and menu
print("--- WELCOME TO OUR CAFE ---")
for item, price in menu.items():
    print(f"{item.capitalize()}: Rs.{price}")
print("---------------------------")

# 3. Take order from the customer
total_bill = 0
order_placed = False

while True:
    choice = input("Enter the item you want to order (or type 'exit' to finish): ").lower()
    
    if choice == "exit":
        break
    
    # Check if the item is present in the menu dictionary
    if choice in menu:
        total_bill += menu[choice]
        print(f"Added {choice.capitalize()} to your cart.")
        order_placed = True
    else:
        print("Sorry, that item is not available.")

# 4. Print the final bill
print("\n---------------------------")
if order_placed:
    print(f"Your Total Bill is: Rs.{total_bill}")
    print("Thank you for ordering!")
else:
    print("You didn't order anything. Have a nice day!")
print("---------------------------")
