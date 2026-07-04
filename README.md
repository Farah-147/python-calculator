print("=" * 40)
print("            PYTHON CALCULATOR")
print("=" * 40)

while True:
    try:
        num1 = float(input("\nEnter the first number: "))
        op = input("Choose an operation (+, -, *, /): ")
        num2 = float(input("Enter the second number: "))
        if op== "+":
            result = num1 + num2
        elif op == "-":
            result = num1 - num2
        elif op == "*":
            result = num1 * num2
        elif op == "/":
            if num2 == 0:
                print("\nError: Division by zero is not allowed.")
                continue
            result = num1 / num2
        else:
            print("\nInvalid operator. Please use +, -, *, or /.")
            continue
        print("\n" + "-" * 40)
        print(f"Result: {num1} {op} {num2} = {result}")
        print("-" * 40)
        again = input("\nWould you like to perform another calculation? (y/n): ").lower()
        if again != "y":
            print("\nThank you for using the Simple Python Calculator!")
            break
    except ValueError:
        print("\n Invalid input. Please enter numeric values only.")
