---
layout: post
title:  "Competitive Programming Cheat Sheet"
date:   2022-12-09 23:17:00
categories: programming
tags: [competitive, cheatsheet, C++, python]
---

# Competitive Programming Cheat Sheet
Finally, I published my cheatsheet for competitive programming. I'm a big fan of websites like [CodinGame](https://www.codingame.com) or [Kattis](https://open.kattis.com/) (and there are so many others!).  
I didn't have much time to take coding challenges but now that Christmas is coming and [Advent of Code](https://adventofcode.com/) has started it's time to also publish my cheat sheet. I will sometimes update this post as I find some new snippets to be useful.  

Latest update: 09.12.2022  

Test speed: [https://www.spoj.com/problems/INTEST/](https://www.spoj.com/problems/INTEST/)  

## Python

```python
for i in range(int(input())):
	line = input()

line = lambda : sys.stdin.readline().strip()
n = int(line())
```

## C++ 

### Template Program

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    return 0;
}
```

- cout.tie(NULL) is not necessary because cin.tie does the job
- Use \n instead of endl

```cpp
// https://www.geeksforgeeks.org/fast-io-for-competitive-programming/
void fastscan(int &number)
{
    //variable to indicate sign of input number
    bool negative = false;
    register int c;
  
    number = 0;
  
    // extract current character from buffer
    c = getchar();
    if (c=='-')
    {
        // number is negative
        negative = true;
  
        // extract the next character from the buffer
        c = getchar();
    }
  
    // Keep on extracting characters if they are integers
    // i.e ASCII Value lies from '0'(48) to '9' (57)
    for (; (c>47 && c<58); c=getchar())
        number = number *10 + c - 48;
  
    // if scanned input has a negative sign, negate the
    // value of the input number
    if (negative)
        number *= -1;
}

ll fastpow(ll base, ll exp, ll mod) {
    ll res = 1;
    while(exp > 0) {
        if((exp & 1) == 1) {
            res = (res * base) % mod;
        }
        base = (base * base) % mod;
        exp /= 2;
    }

    return res % mod;
}

void GetTokens( const std::string &line, std::vector<float> &tokens )
{
    tokens.clear();
    std::stringstream lineStream( line );
    std::string token;
    while ( std::getline( lineStream, token, ' ' ) )
    {
        tokens.push_back( static_cast<float>(stoi( token )) );
    }
}

template <typename T>
void TokenizeStream( std::istream &inputStream, std::vector<T> &tokens )
{
    tokens.clear();
    std::string token;
    while ( std::getline( inputStream, token, ' ' ) )
    {
        tokens.push_back( static_cast<T>(std::stoi( token )) );
    }
}

void GetInputData( std::vector<int> &data )
{
    data.clear();
    std::string line;
    std::getline( std::cin, line );
    std::stringstream lineStream( line );
    std::string token;
    while ( std::getline( lineStream, token, ' ' ) )
    {
        data.push_back( static_cast<int>(stoi( token )) );
    }
}

int CountSubstring( const std::string &str, const std::string &substr )
{
    int count = 0;
    size_t pos = str.find( substr, 0 );

    while ( pos != std::string::npos )
    {
        count++;
        pos = str.find( substr, pos + 1 );
    }

    return count;
}
```