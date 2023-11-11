---
title: "C Tutorials 2"
date: 2023-11-11T00:00:00
author: Cat
tags: [cource,programming,c]
categories: "Programming-in-C"
featured: "false"
type: "intro"
thumbnail: /tutorials/c-20221030/c-icn-20221030.png
articleImage: /tutorials/c-20221030/c-banner-20221030.png
draft: "false"
linktitle: "c-tutorial-2"
---

# C Tutorial Variables:
Today I wanted to talk about variables in C. Different data types in C and how each different type works. 

To create a variable in C the syntax is as follows `typename label`, and to assign a value to this variable `label = value`. Where value is the value you want to give the label.

NOTE these operations can be combined so could declare and assign an int by `int number = 5` 
NOTE label can be whatever you want and typename is one of the types shown below

## Integers:
So what are the basic integer types in C?

1. `char` this is a 8bit variable typically it is used to represent a ASCII or UTF8 character. But it's really just a 8bit number can be used as such in programs.
2. `short` this is a 16bit variable and is just a 16bit integer.
3. `int` this is either a 16bit or 32bit and it depends on your compiler tool chain and target what the size of an int is. But on most modern 64bit systems it's typically 32bit. However I will talk about this more later.
4. `long` this is either a 32-bit or a 64-bit integer in C and again it depends on the compiler and the tool chain used to compile the code.
5. `long long` This is the only type that is certain to be 64bits wide.  

each variable here can be prefixed with either the `signed` or `unsigned` keywords to make the variable signed or unsigned. Signed meaning that it can represent negative and positive numbers but the range is less than unsigned and unsigned being the opposite it can't do negative numbers but has a greater range in positive numbers. However in C variables are signed by default so just `int` is already signed.

So you might have noticed C has variable sized data types so you might wonder how do you know to use the right one well there is a method using the preprocessor. But that is a little complex and not really worth it when with the `stdint.h` header file which provides `uintN_t` where N is the size of the data type. stdint integers are below:

1. `uint8_t & int8_t` These are the unsigned and signed 8bit integers provided through `stdint.h`. The u in uint8_t stands for unsigned.
2. `uint16_t & int16_t` These are the unsigned and signed 16bit integers provided through `stdint.h`.
3. `uint32_t & int32_t` These are the unsigned and signed 32bit integers provided through `stdint.h`.
2. `uint64_t & int64_t` These are the unsigned and signed 64bit integers provided through `stdint.h`.


## Floating Point Integers:
1. `float` floating point integer that takes 4 bytes and has precision up to 6 decimal places.
2. `double` a double is a 8 byte floating point number(get it double as in the size) with precision to 15 decimal places.
3. `long double` A long double is 10 byte floating point number it has precision up to 19 places however it relies on the CPU having a floating point extensions tho most CPUs have those now

## Arrays:
Arrays in C are a collection of elements. Defined by using a C data type and the [] characters after then. Arrays can be indexed with their name and the brackets with a number between them the number is the offset into array. 
```c


    //A warning about arrays
int main() {
    static int array[2];
    static int number;
    
    printf("number %i\n", number);
    array[2] = 30;
    /*If in theroy number was after array 
     *in memory we would have effectively 
     *ovewritten number with this isn't always 
     *going to happen but still possible and shouldn't be done
     */
    printf("number %i\n", number);

    return 0;
}
```
## Pointers:
Pointers in C are a variable that points to location in memory typically to location that contains another variable or collection of variables if the pointer points to an array(NOTE: this array is not a C array but rather an array in the programmatic sense). But a pointer simply points to something else that is located somewhere else in memory. A pointer is defined with a type suffix with a *. Below is an example of an integer pointer. But I will talk more on pointers at a later date as I want to cover them more in depth
```c
int *int_ptr;
```

## Arrays VS Pointers:
Some people say that pointers and arrays are the same in C but they aren't quite the same. They can often be used interchangeable but they can not always be changed. I personally thing about it as an array is not a pointer it is a static collection of elements of the same data type and a C array can't be resized at runtime as they are allocated during compile time directly into the programs executable thus it wasn't allocated. A pointer is dynamic and can change and resize.


## Putting it to use:
Okay that's all we are going to cover for today so I will wrap up with a short program showing an example of these variables in use then leave you with some code and I encourage you to go beyond what I show and experiment/play around with the code. See if you can get name in a variable(tho) that might be tricky as it would use arrays or pointers with the character type. Though if you do decide to try it remember the internet is your friend.

So lets make a basic program that says `"Hey my name is: NAME, I am X years old\n"`

```c

int main() {
    int age = 24;
    
    printf("Hello my name is Cat I am %i\n", age); 

    return 0;
}

```
The above program with will out my name and age at the time of writing.

Thanks is all for now
