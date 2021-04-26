1a.

1) values added: 20
2) final result: 20
3) values added: 20
4) The code on line 13 returns an error because the result variable only has the scope of the if statement (because it was declared by a let). The reference to result on line 13 is out of scope. 
5) The code on line 9 returns an error because the code attempts redefine a const variable from 0 to 20. This is an error because you cannot redefine a const.
6) The code on line 13 returns an error because the reference to result on line 13 is a reference to a variable that is out of scope. It is out of scope because the scope of result is only the if statement (because it was declared with const). Therefore the out of scope reference causes an error to be returned.

1b.

1) The code at line 12 will result in 3 being printed out. Line 12 prints the value of i when the for loop is broken out of. Because it starts at i=0 and goes to i<3, the for loop is broken out of when i reaches the value fo 3 (it no longer satisfies i<3). Therefore, it prints out the number 3. Because i is a var, it can be accesed outside the for loop it was declared.
2) The code at line 13 will result in 150 being printed out. Line 13 will print out the last new price created by the for loop (the new discounted price of the last element in the price array). Because after that i is not < 3, the for loop is broke out of and there is no new value of discountedPrice. Therefore, line 13 prints out the last discountedPrice, which in this case is 150 (50% discounted applied to 300). Because discountedPrice is a var, it can be accesed outside the for loop it was declared. 
3) The code at line 14 will result in 150 being printed out. Line 14 will print out the last final price created by the for loop (the new final price of the last element in the price array). Because after that i is not < 3, the for loop is broke out of and there is no new value of final price. Therefore, line 14 prints out the last finalPrice in the discounted array, which in this case is 150 (50% discount applied to 300, rounded to two decimals). Note, this value is the same as the current discountedPrice because finalPrice just rounds the discountedPrice to two decimal places.
4) The function will return the array [50, 100, 150]. The function will return back an array the same size as the prices array input. This array will be an array with the new prices after the input discount as been applied and the result of the discount application has been rounded to two decimals so it is a legitimate price.
5) The code at line 12 will cause an error because the function call console.log is attempting to access the variable i, which is not in scope. The scope of the i variable is limited to the for loop it was declared, therefore, the attempt on line 12 to access i out of scope causes an error.
6) The code at line 13 will cause an error because the function call console.log is attempting to access the variable discountedPrice, which is not in scope. The scope of the discountedPrice variable is limited to the for loop it was declared, therefore, the attempt on line 12 to access discountedPrice out of scope causes an error.
7) The code at line 14 will result in 150 being printed out. Because finalPrice is declared out of the for loop but within the discountPrices method, it can be accessed anywhere in the discountPrices method. Therefore, it is in the scope of the code at line 14. This prints the value of the finalPrice from the last call of the for loop, which in this case is 150.
8) The function will return the array [50, 100, 150]. Because the discounted is declared out of the for loop but with the discountPrices method, it can be accessed anywhere in the discountPrices method. Therefore, it is in the scope of the return statment at line 16. This prints the value of the discounted array, which in this case is [50, 100, 150], the 3 discounted prices from the original 3 price input.
9) The code at line 11 will cause an error because the function call console.log is attempting to access the variable i, which is not in scope. The scope of the i variable is limited to the for loop it was declared, therefore, the attempt on line 11 to access i out of scope causes an error. Its scope is limited because i was declared as a const instead of a var.
10) The code at line 12 will result in 3 printed out. There is no error because length is declared out of the for loop but within the discountPrices method, it can be accessed anywhere in the discountPrices method. Therefore, it is in the scope of the code at line 12. There is also no error because once length is declared as 3, it is never redeclared again in the code.
11) The function returns the discounted array [50, 100, 150]. It does not error because discounted is declared out of the for loop but within the discountPrices method, it can be accessed anywhere in the discountPrices method. Therefore, it is in the scope of the return statement. It also does not cause any error because although it is a const variable and the value is changed, it is never redeclared, meaning there is no error.

12)
A) student.name
B) student['Grad Year']
C) student.greeting()
D) student['Favorite Teacher'].name
E) student.courseload[0]


13.

A) '32' - The integer 3 maps to directly to its string representation '3' and then is concatenated to '2'
B) 1    - The string '3' maps directly to its integer representation, 3. Then it does 3 - 2.
C) 3    - null is mapped to 0, and then 3 + 0 is done.
D) '3null' - null is mapped to its string representation, 'null', and then is concatenated to '3'.
E) 4       - true is mapped to its integer representation, 1, and then it does 1 + 3.
F) 0       - false is mapped to the integer representation 0 and null is mapped to the integer representation 0. So it does 0 + 0.
G) 3undefined - undefined is mapped directly to its string representation 'undefined', and then concatenated onto '3'. 
H) NaN - NaN means "Not a Number". '3' is mapped to its integer representation, 3. It then does 3 - undefined, which is not a number because you can't do math with undefined.


14.

A) true - '2' is mapped to the integer representation 2, and then it does 2 > 1. 
B) false - Because both are strings, it compared ASCII values of the string. Because it goes index by index, it compares '2' to '1' first, which is false because '2' is not less than '1'. 
C) true - Compares loose equality. It converts '2' to 2, and then compares 2 == 2, which is true.
D) false - Compares strict equality, meaning they must be the same type and value. Because one is an int and one is a string, they are not equal by ===.
E) false - Converts true to 1 and then compares it to 2 by doing 1 == 2, which is false.
F) true - On any input that is not null or undefined, the Boolean function outputs true. Therefore, Boolean(2) outputs true, and then it does true === true, which is true because they are equal in value and type.

15.

The == operator tests for loose equality, meaning it does type coercion. This means it tries to convert the values to a common type and then compares them. This means two objects that do not have the same type can evaluate to true using the == operator. The === operator tests for strict equality, meaning that the two things being compared must have the same value and type. This means that there is no type coercion and two values of different types can never be equal (for example, 2 === '2' is false).

16.

See part1b-question16.js

17.

The result is the array [2,4,6]. modifyArray takes in the array [1,2,3] and the method doSomething, which multiplies an input integer by 2. It then uses a for loop to itterate through the array [1,2,3]. For each value in the array, it inputs the value to the doSomething function and stores the result of calling the doSomething function into a new array. It then returns this modified array. Therefore, it returns [2,4,6], which is basically equivalent to [doSomething(1), doSomething(2), doSomething(3)].

18.

See part1b-question18.js

19.

1
4
3
2

