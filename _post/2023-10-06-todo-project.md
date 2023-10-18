
I started off by creating two variables, one containing a list and another containing an empty string. This will be really useful later when we initiate branching conditionals.

![A pic of code](/assets/sc1.png)

Next, I worked on the base of the whole project which was initiating a while loop. In order to make this project user-friendly, I needed to make a way for the loop to stop when the user wishes for it to. I did this by using the empty "Choices" variable That I created earlier and making it so that when the choices option appears, the user can just type "stop" to end the statement. This happens because the condition for the while loop is that it'll proceed with its iterations while the "Choices" variable is NOT equivalent to the strings "Stop", "stop", or "3". There are 2 different stops because computers are very specific with spelling so I put one in lowercase so that the mechanics are more user-friendly.

![A pic of code](/assets/sc2.png)

I started off by showing simple print statements that tell the user their current Todos within their list. The word todo is put within the print statement since that's the name of our list.


print('Your current todos are:')
print(Todo)


After that, I started working towards giving the user the ability to choose whether they want to add to the list, delete from the list, or stop the statement altogether. This is done through a simple input statement connecting to our empty "Choices" variable.


    Choices = input('Please select an option. Current choices are "Add" : 1, "Delete" : 2 or "Stop" : 3 to stop:  ')


After the previous statement, I added another input statement connected to the variable "Addtodo", which allows them the type in whatever they may want to add to their list. Afterward, the item will be added to its list via the variable and a statement known as "append", which adds an item chosen to the very end of the list.


    Addtodo = input('Please type in something to add to your todo list: ')
    Todo.append(Addtodo)
    print()
    print(Addtodo + ' has been added!')
    print()


This segment is then repeated with the delete & add options, but the noticeable distinction is that the "if" statements are now "elif" statements.


Delete Option 
elif Choices == "Delete" or Choices == 'delete' or Choices == "2" :

Stop Option
elif Choices == "Stop" or Choices == 'stop' or Choices == "3" :



For the delete option, there will be an input statement that asks which you'd like to delete. The list will be scaled by numbers starting from the value of 1 as the first one. Once a number is said in the input statement, the input data type is then converted to an integer allowing it to be added to mathematical statements. The input variable ("Deltodo") is then subtracted by one inside the list todo using the "del" statement.


    del Todo[Deltodo - 1]
    print("Your selected statement has been deleted!")
    print()  


    Please select an option. Current choices are "Add": 1, "Delete": 2, or "Stop" : 3 to stop:  2
    Please select the number for the item in the list you'd like to remove: 1
    Your selected statement has been deleted!



The last part of the choice segment is the "Stop" function. The purpose of this statement, as previously mentioned, is to stop the loop once you're finished. this was the easiest part of the choices segment since it just required 3 conditionals under an elif.



    elif Choices == "Stop" or Choices == 'stop' or Choices == "3" :
    print('Statement is now stopping')
    print()



An else statement to end the ifs and elifs. This is added to ensure that something can happen if none of my conditions are met. If the conditional goes to the else, the code will loop again.


    elif Choices == "Stop" or Choices == 'stop' or Choices == "3" :
    print('Statement is now stopping')
    print()



    Todo = []
    Choices = ''


    while Choices != 'Stop' and Choices != '3' and Choices != 'stop' :


    print()
    print('Your current todos are:')
    print(Todo)
    print()

    Choices = input('Please select an option. Current choices are "Add" : 1, "Delete" : 2 or "Stop" : 3 to stop:  ')
    print()


    if Choices == "Add" or Choices == 'add' or Choices == "1" :

    Addtodo = input('Please type in something to add to your todo list: ')
    Todo.append(Addtodo)
    print()
    print(Addtodo + ' has been added!')
    print()


    elif Choices == "Delete" or Choices == 'delete' or Choices == "2" :

        Deltodo = int(input("Please select the number for the item in the list you'd like to remove: "))

        del Todo[Deltodo - 1]
        print("Your selected statement has been deleted!")
        print()


    elif Choices == "Stop" or Choices == 'stop' or Choices == "3" :
        print('Statement is now stopping')
        print()


    else :
        print('The answer chosen is invalid.')
        print()