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

