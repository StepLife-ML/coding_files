#Password Generator Project
import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

#Eazy Level - Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91
#python random.randint()
#for i in range
random_letters = 0
random_symbols = 0
random_numbers = 0
total_letters = ""
total_symbols = ""
total_numbers = ""
random_digit = 0
complete_password = ""

for i in range(nr_letters):
    random_letters = random.randint(0,len(letters)-1)
    total_letters += letters[random_letters]
    
for i in range(nr_symbols):
    random_symbols = random.randint(0,len(symbols)-1)
    total_symbols += symbols[random_symbols]

for i in range(nr_numbers):
    random_numbers = random.randint(0,len(numbers)-1)
    total_numbers += numbers[random_numbers]
    
all_password = (total_letters + total_symbols + total_numbers)
split_list = list(all_password)
maximum_digit = int(input("How many digit of password that you want to generate?"))
                    
for i in range(maximum_digit):
    random_digit = random.randint(0,len(split_list)-1)
    complete_password += split_list[random_digit]
print(complete_password)


#Hard Level - Order of characters randomised:
#e.g. 4 letter, 2 symbol, 2 number = g^2jk8&P
