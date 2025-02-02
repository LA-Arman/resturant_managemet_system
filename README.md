menu = {
    "pizza": 50,
    "pasta": 60,
    "burger": 70,
    "salad": 30,
    "water": 20,
    "coffee": 50,
}

print("Welcome to Arman Restaurant!")
print("\nMENU")
for item, price in menu.items():
    print(f"{item.capitalize()}: RS {price}")

order_total = 0
ordered_items = []

while True:
    items = input("\nEnter the items you want to order (separate by commas): ").lower().split(',')
    
    for item in items:
        item = item.strip()  # Remove extra spaces
        if item in menu:
            order_total += menu[item]
            ordered_items.append(item.capitalize())
            print(f"{item.capitalize()} has been added to your order.")
        else:
            print(f"Sorry, {item.capitalize()} is not available in our menu.")

    another_order = input("\nDo you want to add more items? (YES/NO): ").strip().lower()
    if another_order == "no":
        break
    elif another_order != "yes":
        print("Invalid response. Please enter YES or NO.")

# Display final order summary
print("\nOrder Summary")
print(f"Items Ordered: {', '.join(ordered_items)}")
print(f"Total Amount: RS {order_total}")
print("\nThank you for dining with us! Have a great day!")



# resturant_managemet_system
i have make this resturant menu and bill screen using some basic concept of python i have a learned a lot of thing and face challenges and error but i learned a lot from it using this projet
i hope next time i make better than from it. 
