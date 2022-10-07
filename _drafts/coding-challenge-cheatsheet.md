# Coding Challenge Sheatsheet

## Python

```python
for i in range(int(input())):
	line = input()

line = lambda : sys.stdin.readline().strip()
n = int(line())
```

## C++

- [ ] implement python lambda solution. Wtf? Add more comment next time!
- [ ] ignore cin
- [ ] use getline
- [ ] templated tokenizer

https://www.geeksforgeeks.org/fast-io-for-competitive-programming/  
https://codeforces.com/blog/entry/8080?locale=ru  
https://github.com/Kattis/kattio/blob/305f1b012d8d6f3a15ba51fcfcffec09529c06af/fast_io.cpp  
https://github.com/Maycon708/Maratona/blob/68afecc28f9a46a50ab33f7dbeb52218ada778d0/URI/2042%20-%20Fof%C3%A3o%20da%20P%C3%A9rsia.cpp  

```cpp
ios::sync_with_stdio(false);
cin.tie(NULL);
cout.tie(NULL);

ll readint(){
    char r;
    bool start=false,neg=false;
    ll ret=0;
    while(true){
        r=getchar();
        if((r-'0'<0 || r-'0'>9) && r!='-' && !start){
            continue;
        }
        if((r-'0'<0 || r-'0'>9) && r!='-' && start){
            break;
        }
        if(start)ret*=10;
        start=true;
        if(r=='-')neg=true;
        else ret+=r-'0';
    }
    if(!neg) return ret;
    else return -ret;
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