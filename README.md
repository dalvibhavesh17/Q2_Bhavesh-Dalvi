print("Enter a password which is of minimum 8 characters and it has atleast 1 Uppercase, 1 lowercase, 1 digit, 1 character")
password='Bha@7%'
strong=0
weak=0
charac=['!','@','#','$','%','&','*',':',';']
if len(password)>=8:
    for i in password:
        if i.isupper():
            strong+=1
            break
    else:
        weak+=1
    for i in password:
        if i.islower():
            strong+=1
            break
    else:
        weak+=1
    for i in password:
        for j in range(0,10):
            if i==str(j):
                strong+=1
                break
    else:
        weak+=1
    for i in password:
        for j in charac:
            if j==i:
                strong+=1
                break
    else:
        weak+=1

    if weak > 0:
        print("the password is weak")
    else:
        print("the password is strong")
else:
    print("the password does not have a minimum of 5 letters")
print(strong)
print(weak)
