# Calculator
A calculator to calculate simple equations 

#calculator 

#Add
def add(n1, n2):
  return n1 + n2

#Subtract
def subtract (n1, n2):
  return n1 - n2

#Multiply
def multiply (n1, n2):
  return n1 * n2

#Divide:
def divide(n1, n2):
  return n1 / n2

operations = {
  "+": add,
  "-": subtract, 
  "*": multiply, 
  "/": divide   
}

num_1 = int(input("What is the first number? "))
num_2 = int(input("What is the second number? "))
for symbol in operations:
  print(symbol)
operation_symbol = input("Pick an operation from the line above: ")

continue_calculation = True

calculation_function = operations[operation_symbol]
first_answer = calculation_function(num_1, num_2)
print(f"{num_1} {operation_symbol} {num_2} = {first_answer}")

while continue_calculation == True:
  choice = input("do you want to continue with another calculation? Y or N: ")
  if choice != "Y":
    continue_calculation = False
    break 
  next_operation = input("choose another operation: ")
  next_number = int(input("choose another number: "))
  calculation_function = operations[next_operation]
  next_answer = calculation_function(first_answer, next_number)
  print(f"{first_answer} {next_operation} {next_number} = {next_answer}")
  first_answer = next_answer
  

  
