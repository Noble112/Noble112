class Calculator:
    def __init__(self):
        self.result = 0

    def add(self, number):
        self.result += number
        return self.result

    def subtract(self, number):
        self.result -= number
        return self.result

    def multiply(self, number):
        self.result *= number
        return self.result

    def divide(self, number):
        if number == 0:
            raise ValueError("Division by zero is not allowed.")
        self.result /= number
        return self.result


def calculator_operations():
    calc = Calculator()
    while True:
        print("Select operation:")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Exit")

        choice = input("Enter choice(1/2/3/4/5): ")

        if choice in ('1', '2', '3', '4'):
            number = float(input("Enter number: "))

            if choice == '1':
                print("Result: ", calc.add(number))
            elif choice == '2':
                print("Result: ", calc.subtract(number))
            elif choice == '3':
                print("Result: ", calc.multiply(number))
            elif choice == '4':
                print("Result: ", calc.divide(number))
        elif choice == '5':
            print("Exiting the program.")
            break
        else:
            print("Invalid Input")


if __name__ == "__main__":
    calculator_operations()
