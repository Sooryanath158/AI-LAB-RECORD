male(peter).
male(john).
male(chris).
male(kevin).

female(betty).
female(jeny).
female(lisa).
female(helen).

parentOf(chris, peter).
parentOf(chris, betty).
parentOf(helen, peter).
parentOf(helen, betty).
parentOf(kevin, chris).
parentOf(kevin, lisa).
parentOf(jeny, john).
parentOf(jeny, helen).

father(X, Y) :- male(Y), parentOf(X, Y).
mother(X, Y) :- female(Y), parentOf(X, Y).

grandfather(X, Y) :- male(Y), parentOf(X, Z), parentOf(Z, Y).
grandmother(X, Y) :- female(Y), parentOf(X, Z), parentOf(Z, Y).

brother(X, Y) :- male(Y), parentOf(X, Z), parentOf(Y, W), Z == W.
sister(X, Y) :- female(Y), parentOf(X, Z), parentOf(Y, W), Z == W.
OUTPUT:
male(peter)
true
father(chris,peter)
true
false
father(chris,betty)
false
grandfather(kevin,peter)
tru
false
grandfather(jenny,peter)
true
false
mother(chris,x)
x=betty
brother(peter,chris)
true
false
brother(helen,chris)
ture
false
grandmother(X,Y)
x=kevin
y=betty
x=jenny
y=betty
