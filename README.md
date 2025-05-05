# cs186-428


# I  
``` cpp

#include <iostream>
#include <vector>
using namespace std;


void Print_every_other(int low , const int hight) {
    if(low <= hight) {
        cout << low << endl;
        Print_every_other(low+2,hight);
    }




}
int main() {
    Print_every_other(0,10);

    return 0;
}

```

# II 
The recursions function will never stop .


# III 
```cpp


#include <iostream>
#include <vector>
using namespace std;


int Sum(int low , const int hight) {
    if (hight == low){
        return hight;
    } else{
        return (hight + Sum(low,hight-1));
    }




}
int main() {


    return 0;
}

```

# IV 
``` cpp
using namespace std;

struct Node {
    bool isNumber;
    int  value{};
    vector<Node> list;


    Node(int v )
            : isNumber(true), value(v) {}

    Node(initializer_list<Node> a)
            : isNumber(false), list(a) {}
};


void printAll( Node n)
{
    if (n.isNumber) {
        cout << n.value << ' ';
    } else {
        for ( auto m : n.list)
            printAll(m);
    }
}
int main()
{

    Node array{
            1, 2, 3,
            {4, 5, 6},
            7,
            {
                    8,
                    {9, 10, 11, {12, 13, 14}},
                    {15, 16, 17, 18, 19,
                     {20, 21, 22,
                      {23, 24, 25, {26, 27, 29}},
                      30, 31},
                     32},
                    33
            }
    };
    printAll(array);
    cout << '\n';
    return 0;
}

```
## video


