# Python Gamma projects

# Exercise 1 



#   Character input

name = input("What is your name: ")
age = int(input("How old are you: "))
year = str((2014 - age)+100)
print(name + " will be 100 years old in the year " + year)

# output is 

What is your name: Fawad
How old are you: 5
Fawad will be 100 years old in the year 2109



# Exercise 2


# odd or Even 

 num = int(input("give me a number to check: "))
check = int(input("give me a number to divide by: "))

if num % 10 == 0:
    print(num, "is a multiple of 4")
elif num % 2 == 0:
    print(num, "is an even number")
else:
    print(num, "is an odd number")

if num % check == 0:
    print(num, "divides evenly by", check)
else:
    print(num, "does not divide evenly by", check)
    
    # Output is
    
give me a number to check: 4
give me a number to divide by: 2
4 is an even number
4 divides evenly by 2

give me a number to check: 9
give me a number to divide by: 3
9 is an odd number
9 divides evenly by 3


# Exercise 3

# List less then ten


myList = [1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]


for element in myList:
    if int(element) < 5:
        print(element)


#Extras
newList = [ e for e in myList if int(e) < 5 ]


print(newList)


def findLessNumber(array, number):
    for element in array:
        if int(element) < number:
            print(element)



num = int(input('Type one number to compare to the list:'))

findLessNumber(myList,num)


# Output is

1
1
2
3
[1, 1, 2, 3]
Type one number to compare to the list:78
1
1
2
3
5
8
13
21
34
55




# Exercise 4


# Divisor



num = int(input("Please choose a number to divide: "))

listRange = list(range(1,num+1))

divisorList = []

for number in listRange:
    if num % number == 0:
        divisorList.append(number)

print(divisorList)


# Output is

Please choose a number to divide: 15
[1, 3, 5, 15]



# Exercise 5


# List Overlap


a = [12,12,14,14,15,17,18,19,20]
b = [12,14,17,18,21,32,34,45,56]
list(set(a) & set(b))

# Output is

[17, 18, 12, 14]



import random

def list_overlap():

	a = random.sample(range(10), 3)
	b = random.sample(range(10), 3)
	for i in a:
		if i in b:
			print(i)

list_overlap()

# Output is

4


# Exercise 6


# String list

def reverse(word):
	x = ''
	for i in range(len(word)):
		x += word[len(word)-1-i]
	return x

word = input('give me a word:\n')
x = reverse(word)
if x == word:
	print('This is a Palindrome')
else:
	print('This is NOT a Palindrome')

# Output is 

give me a word:
-9
This is NOT a Palindrome


give me a word:
h
This is a Palindrome


give me a word:
7
This is a Palindrome


# Exercise 7

# List Comprehensions


a = [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
b = [element for element in a if element % 2 == 0]
print(b)


# Output is


[4, 16, 36, 64, 100]



# Exercise 8

# Rock Paper Scissors


import sys

user1 = input("What's your name?")
user2 = input("And your name?")
user1_answer = input("%s, do yo want to choose rock, paper or scissors?" % user1)
user2_answer = input("%s, do you want to choose rock, paper or scissors?" % user2)

def compare(u1, u2):
    if u1 == u2:
        return("It's a tie!")
    elif u1 == 'rock':
        if u2 == 'scissors':
            return("Rock wins!")
        else:
            return("Paper wins!")
    elif u1 == 'scissors':
        if u2 == 'paper':
            return("Scissors win!")
        else:
            return("Rock wins!")
    elif u1 == 'paper':
        if u2 == 'rock':
            return("Paper wins!")
        else:
            return("Scissors win!")
    else:
        return("Invalid input! You have not entered rock, paper or scissors, try again.")
        sys.exit()

print(compare(user1_answer, user2_answer))


# Output is

What's your name?Fawad
And your name?Jawad
Fawad, do yo want to choose rock, paper or scissors?rock
Jawad, do you want to choose rock, paper or scissors?paper
Paper wins!

# another output


What's your name?Immal
And your name?Kashi
Immal, do yo want to choose rock, paper or scissors?scissors
Kashi, do you want to choose rock, paper or scissors?rock
Rock wins!



#  Exercise 9


#  Guessing Game One


import random

rd = random.randint(1,9)
guess = 0
c = 0
while guess != rd and guess != "exit":
    guess = input("Enter a guess between 1 to 9")

    if guess == "exit":
        break

    guess = int(guess)
    c += 1

    if guess < rd:
        print("Too low")
    elif guess > rd:
        print("Too high")
    else:
        print("Right!")
        print("You took only", c, "tries!")
input()

#  Output is


Enter a guess between 1 to 91
Too low
Enter a guess between 1 to 92
Too low
Enter a guess between 1 to 93
Too low
Enter a guess between 1 to 94
Too low
Enter a guess between 1 to 95
Too low
Enter a guess between 1 to 96
Too low
Enter a guess between 1 to 97
Too low
Enter a guess between 1 to 97
Too low
Enter a guess between 1 to 98
Right!
You took only 9 tries!
9
