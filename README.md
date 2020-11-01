alphabet = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ"
first = input("Введите первое слово: ")
second= input("Введите второе слово: ")
third= input("Введите третье слово: ")
passw=""
passw+=alphabet[(alphabet.index(first[0]) + 1 % (len(alphabet)-1))]
passw+=alphabet[(alphabet.index(first[0]) + 2 % (len(alphabet)-1))]
passw+=alphabet[(alphabet.index(second[2]) - 1 % (len(alphabet)-1))]
if len(third)% 2 != 0:
    passw+=alphabet[(alphabet.index(third[3]) + 1 % (len(alphabet) - 1))]
else:
    passw+=alphabet[(alphabet.index(third[len(third)//2]) - 1 % (len(alphabet) - 1))]
passw+=alphabet[(len(first)+len(second) % 26)]
print(passw.lower())
import getpass
import sys

if sys.stdin.isatty():
    p = getpass.getpass('Using getpass: ')
else:
    print('Using readline')
    p = sys.stdin.readline().rstrip()
if p==passw.lower():
    print("Success")
else:
    print("Print bad password")
