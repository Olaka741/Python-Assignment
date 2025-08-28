# Python-Assignment

def simple_calculator():
    print("🧮 Simple Python Calculator")
    print("=" * 30)
    
    # Get inputs
    try:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
        print("\nAvailable operations: +, -, *, /")
        operation = input("Choose an operation: ").strip()
        
        # Calculate and display result
        if operation == '+':
            result = num1 + num2
            operator = "+"
        elif operation == '-':
            result = num1 - num2
            operator = "-"
        elif operation == '*':
            result = num1 * num2
            operator = "*"
        elif operation == '/':
            if num2 == 0:
                print("❌ Error: Cannot divide by zero!")
                return
            result = num1 / num2
            operator = "/"
        else:
            print("❌ Invalid operation! Please choose from +, -, *, /")
            return
        
        # Display the result
        print(f"\n✅ Result: {num1} {operator} {num2} = {result}")
        
    except ValueError:
        print("❌ Error: Please enter valid numbers!")
    except Exception as e:
        print(f"❌ An unexpected error occurred: {e}")

# Run the calculator
simple_calculator()
