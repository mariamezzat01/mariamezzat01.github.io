# Const 

Const keyword in C++ or C is used to make the value of elements constant. It can be used in multiple contexts such as:

### 1-	Variables 
If you make any variable as constant, using const keyword, you cannot change its value. Also, the constant variables must be initialized while they are declared.

For example:
```
int main
{
    const int i = 10;
    const int j = i + 10;     // works fine
    i++;    // this leads to Compile time error   
}
```
**Code explanation:**
In the above code we have made i as constant, hence if we try to change its value, we will get compile time error. Though we can use it for substitution for other variables.


### 2-	Pointers with const keyword in C++ 
There are 2 ways that pointers can be associated with const keyword, either by pointing to a constant variable or the pointer itself be a constant

a)	```const int* u; ```   OR   ``` char const* v;```
this means that the pointer points to a constant variable which is very useful as it can be used to make any array or string  immutable

b)	```int x = 1;
int* const w = &x;```
here the pointer w will always point to variable x, however, the value of x can be changed later on, which is very useful in storage that can be changed by value but not moved in memory as the pointer will always point to the same memory location.

c) ```const int* const x;```
Const pointer pointing to const variable.

### 3-	Const Function Arguments and Return types
We are able to make the return type or arguments of a function as const which will make them immutable.

For example:
```
void f(const int i)
{
    i++;    // error
}

const int g()
{
    return 1;
}
```
### 4-	Defining Class Data members as const
We may define data variables using const keyword but they are initialized in the constructor not during declaration.

For example:
```
class Test
{
    const int i;
    public:
    Test(int x):i(x)
    {
        cout << "\ni value set: " << i;
    }
};

int main()
{
    Test tx(10);
    Test sx(20);
}
```
Code explanation:
Here i is a const data member, so in every object an independent copy will be present as it is initialized with each object using the constructor and once initialized, its value cannot be changed.

### 5-	Defining Class Object as const
When an object is declared using const keyword its data members can never be changed

For example:
```
const class_name object;
```
### 6-	Defining class’s member function as const
 const member functions never modifies data members in an object.

For example:
```
return_type function_name() const;
```

# & Operator 
The & operator  can be used as a reference variable to extract the address of variable as the below example:
```&variable;```

and also can create reference called ref to variable
```Type& ref = variable;```

it can also be used as Logical AND which True only if all the operands are true.
```expression1 && expression2```


