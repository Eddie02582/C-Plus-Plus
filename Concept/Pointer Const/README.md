# Const Pointer

<ul>
    <li>const int *p</li>
    <li>int const *p</li>
    <li>int *const p</li>
    <li>const int *const p</li>
</ul>


       
## const int *p

const 修試int *p 為常量,所以 *p 為const,但是p可以改變            
            
```c++
    const int  a= 42;
    const int *p = &a; // we can change p; const is low-level,can not change *p 
    int b = 5;
    p = &b ;
    cout << *p << endl;
```
            
## int const *p     
const 修試*p,*p為const,但是p可以改變,所以const int * 等於 int const *
   
```c++
    const int  a= 42;
    int const*p = &a; // we can change p; const is low-level,can not change *p 
    int b = 5;
    p = &b ;
    //*p = 3; //not allow
    cout << *p << endl;
    return 0;
```

## int *const p 
const 修試p,p為const,但是p*可以改變
   
```c++
    //const int a = 42 not allow
    int  a= 42;
    int *const p = &a; 
    *p = 3; 
```



## const int *const p
p and *p都為const

```c++
    int i = 0;
    const int *const p = &i;
    int c = 5;
    //p = &c; not allow
    //*p = 5; not allow
```


## int constexpr  *q / constexpr int *q
q is a constant pointer to the const int i

```c++
    int i = 0;
    constexpr int  *q = nullptr;
    *q = 5;
    //p = &i; not allow
   
```

















