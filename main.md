```
import re

password = input('Enter a password: ')

def strong(x):
    
    fine = True
    
    if len(x) < 8:
        print('The password must contain at least 8 characters. ')
        fine = False
        x = input('Enter a password: ')
        strong(x)
    if not re.search(r'[A-Z]', x):
        print('The password must contain at least one uppercase letter.')
        fine = False
        x = input('Enter a password: ')
        strong(x)
    if not re.search(r'[a-z]', x):
        print('The password must contain at least one lowercase letter.')
        fine = False
        x = input('Enter a password: ')
        strong(x)
    if not re.search(r'[0-9]', x):
        print('The password must contain at least one digit.')
        fine = False
        x = input('Enter a password: ')
        strong(x)
    if fine is True:
        print('Valid password.')

strong(password)


```
