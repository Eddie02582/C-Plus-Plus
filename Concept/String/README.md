# String


## Initialize

```c++
    string s1;
    string s2 = s1;
    string s2 = (s1);
    string s3 = "hiya";
    string s3 = ("hiya");
    string s4(10, 'c');
    string s5 = string (10, 'c');
```



## operator +

### Adding Two strings

```c++
    string s1 = "hello", s2 = "world"; 
    string s3 = s1 + s2;
    s1 += s2;  
    string s5 = s1.append(s2);     // use append add string
```
 
### Adding Literals and strings 
When we mix strings and string or character literals, at least one operand to each + operator must be a string type
,以下範例s5,s6為錯誤

```c++
    string s1 = "hello", s2 = "world"; 
    string s3 = s1 + ", " + s2 + '\n';
    string s4 = s1 + ", ";     
    string s5 = "hello" + ", ";        // error: no string operand  
    string s6 = s1 + ", " + "world";
    string s7 = "hello" + ", " + s2;   // error: can't add string literals    
    string s8 = s1.append("123");     // use append add string
```
可以將s5修改為
```c++
    string s5 = string("hello") + ", ";// ok:adding a string and a literal
    string s5 = "hello" + string(", ");// ok:adding a string and a literal
```
將s7修改為
```c++
    string s9 = "hello" + (", " + s2); //adding a literal and a string 
```



## for loop

```c++
    vector<int> v = {1,2,3,4,5};
    
    
    for(auto &n :v)
        cout << n << " ";
    cout<<endl;
    
    for(auto it = v.begin();it != v.end();it++)
        cout << *it << " ";
    cout<<endl; 
    
    for(int i = 0;i < v.size();i++)
        cout << v[i] << " ";
    cout<<endl; 
    
    return 0;
```
