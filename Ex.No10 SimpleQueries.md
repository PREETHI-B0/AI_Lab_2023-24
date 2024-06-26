# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE:1/04/2024                                                                            
### REGISTER NUMBER : 212221220040
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5: Prolog interpreter shows the output and return answer. <br> 
 Step 6:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br>
Convert into clause form and Prove that John like Apple by using Prolog. <br>
~~~
### Program:
likes(john,X):-
	food(X).
eats(bill,X):-
	eats(sue,X).
eats(Y,X):-
	food(X).
eats(bill,peanuts).
food(apple).
food(chicken).
food(peanuts).
~~~
### Output:
![image](https://github.com/PREETHI-B0/AI_Lab_2023-24/assets/136311079/12337c87-7cbe-469e-a1d0-34444b50482e)

### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 
~~~
### Program:
likes(steve,X):-
     easycourse(X).
hard(sciencecourse).
easycourse(X):-
          course(X,dept(havefun)).
course(bk301,dept(havefun)).
~~~
### Output:
![318403830-39a87dcb-c856-44c1-8339-68da5d2e1ded](https://github.com/PREETHI-B0/AI_Lab_2023-24/assets/136311079/3aea242f-7f79-44bb-a933-a41fdaeb9499)
### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
~~~
### Program:
criminal(X):-
	american(X),
	weapon(Y),
	hostile(Z),
	sells(X,Y,Z).
weapon(Y):-
    missile(Y).
hostile(Z):-
    enemy(Z,X).
missile(m).
owns(nano,m).
enemy(nano,america).
american(west).
~~~
### Output:
![318403896-6415e220-3f91-4d66-baa1-b1fd7597647a (1)](https://github.com/PREETHI-B0/AI_Lab_2023-24/assets/136311079/cde1c68b-eb2b-4e88-8413-3867aefad6f5)
### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
