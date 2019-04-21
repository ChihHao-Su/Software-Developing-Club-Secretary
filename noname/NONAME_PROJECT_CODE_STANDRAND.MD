# SSRX NONAME PROJ. CODE STD.
For boost team-work, speed up developing of the proj.
## LOCAL VAR. (vars. in func.)
```CPP

void example(){
    string str = "asdfasdf";    // #1
    auto aa = aa();             // #2.1
    auto &bs = sb();            // #2.2
}
```
- #### To CONSTRACT an obj.:
- - If the object can be constract with 1 param. write code like that:
```CPP
typename varname = init_value;
```
Just like what #1 looks like.

- - Else, write code like that:
```CPP
typename varname(init_value1, init_value2, init_value3, ...);
```

- #### To GET THE RETURN VALUE OF A FUNC.(name as "A"):
- - If func. A returns a value-like var(see "value-like vars.".), write code like that:
```CPP
    auto varname = funcname(params);
```
Just like what #2.1 looks like.

- - Else, write code like that:
```CPP
    auto &varname = funcname(params);
```

------------------------------------------------------------------------------
## MENBER VAR. (vars. in class.)
```CPP
class Wsb
{
    string Name;
    int Age;
    bool IsMan;
    
    spGameObject Father;    //#1.1
    spGameObject Mother;    //#1.2
    
};
```
- - If the object returns a value-like var(see "value-like vars.".), write code like that:
```CPP
    typename_of_smartpointer_of_obj varname;
```
Just like what #1.1 and #1.2 looks like.  
Generally, the typename of smartpointer of an obj. is like spXXXXXXXX.
-------------------------------------------------------------------------------
## MENBER FUNC. (funcs. in class)
```CPP
// wsb.h
class Wsb
{
public:
    void Eat(GameItemContainer &food);  //#2
    void SetName(string time);

private:
    int hp;
    string name;
};


//wsb.cxx
void Wsb::Eat(GameItemContainer &food){
    this->hp += food.GetItem()->hp;
    food.SetItem(nullptr);
}

void Web::SetName(string time){
    this->hp -= time*1000;
}

```
- - If the param. of func. is a value-like var(see "value-like vars.".), write code like that:
```CPP

```

-------------------------------------------------------------------------------
## 
