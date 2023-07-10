# python_project
import random
def gameWin(comp,you):
    if comp==you:
        return None
    elif comp=='s':
        if you=='w':
            return False
    elif you=='g':
        return True
    elif comp=='w':
       if you=='g':
           return False
       elif you=='s':
           return True
    elif comp=='g':
        if you=='s':
            return False
        elif you=='w':
            return True
     
randNo=random.randint(1,3)
print(randNo)

if randNo==1:
    comp='s'
elif randNo==2:
    comp='w'
elif randNo==3:
    comp='g'

print("Comp turn: Snake(s)  Water(w)  Gun(g)?\n")
you=input("Player's turn: Snake(s)  Water(w)  Gun(g)?\n")

a=gameWin(comp,you)

print(f"computer choose {comp}")
print(f"You Choose {you}")
if a==None:
    print("The game is tie!")
elif a==True:
    print("You Win!")
else:
    print("You Lose!")
