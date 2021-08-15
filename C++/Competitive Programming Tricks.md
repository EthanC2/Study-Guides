# Competitive Programming Tricks
A collection of clever optimizations/hacks that will give you an edge in a competition. <br />
A lot of these work regardless of language.

## Determining Parity
The parity of a number (whether it is even or odd) can be quickly determined using the bitwise AND operator (&). <br />
Any odd number `& 1` is 1 (true) and any even number `& 1` is 0 (false). 

```C++
int num = 65535;

if (num & 1)  //True
    cout << "The number is odd\n";
```

## Fast Multiplication/Division
You can shift the bits of a number with the _<<_ and _>>_ operators to perform fast multiplication and divsion with powers of 2. <br />
A number `<< n` is the equivalent of multiplying that number by _2^n_. The same goes for division with the _>>_ operator.

```C++
//Multiplication
cout << (12 << 1) << '\n';   // 12 * (2^1) == 24
cout << (12 << 3) << '\n';  //  12 * (2^3) == 94  
    
//Division
cout << (12 >> 1) << '\n';  // 12 / (2^1) == 6
cout << (12 >> 2) << '\n'; //  12 / (2^2) == 3
```