"Bannana, Apple, Kiwi, Grapefruit" 이런 식으로 Input이 들어오면 어떻게 해야할까.

```C++
#include <iostream>

#include <bits/stdc++.h>

  
  
  

using namespace std;

  

vector<string> split(const string& input, string delimiter){

    vector<string> result;

    auto start = 0;

    auto end = input.find(delimiter);

    while(end != string::npos){

        result.push_back(input.substr(start, end -start));

        start = end + delimiter.size();

        end = input.find(delimiter,start);

    }

    result.push_back(input.substr(start));

    return result;

}

  
  

int main(){

    string inputState = "Apple,Bannana,Grape,Kiwi";

    vector<string> fruits = split(inputState,",");

    for(const string& fruit:fruits){

        cout << fruit << endl;

    }

}
```