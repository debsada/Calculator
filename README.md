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

answer = operations[operation_symbol](num_1, num_2)

print(f"{num_1} {operation_symbol} {num_2} = {answer}")
  
