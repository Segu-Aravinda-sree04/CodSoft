def addition(a, b):
  return a + b

def subtraction(a, b):
  return a - b

def multiplication(a, b):
  return a * b

def division(a, b):
  if b != 0:
    return a / b
  if b == 0:
    print("Error. Division by zero is not possible.")

def Calculator():
  print("Simple Calculator")
  while True:
    try:
      num1 = float(input("Enter the first number : "))
      num2 = float(input("Enter the second number : "))
      print("OPERATIONS")
      print("1.Addition")
      print("2.Subtraction")
      print("3.Multiplication")
      print("4.Division")

      operation = input("Select any ONE operation[1/2/3/4/] : ")

      if operation == "1":
        answer = addition(num1, num2)
        print("Answer = ", answer)

      elif operation == "2":
        answer = subtraction(num1, num2)
        print("Answer = ", answer)

      elif operation == "3":
        answer = multiplication(num1, num2)
        print("Answer = ", answer)

      elif operation == "4":
        answer = division(num1, num2)
        print("Answer = ", answer)

      else:
        print("Invalid. Select a valid operation[1/2/3/4].")

      another_calculation = input("Do you want to perform another calculation?[yes/no]:")
      if another_calculation.lower() == 'yes':
        continue
      else:
        print("EXITING...")
        break

    except ValueError:
      print("Invalid input.Please enter valid numbers.")
    except Exception as e:
      print("Error occured",e)

if __name__ == "__main__":
    Calculator()
