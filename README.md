# Hash_Table

Write a code in C++/Python to improve the search operation efficiency O(N) to $O(1).

C++:
  
    #include <iostream>
    #include <unordered_map>
    
    using namespace std;
    
    int main()
    {   
    int array[] = {200, 400, 100, 50, 350};
  
    int num = sizeof (array) / sizeof (array[0]);
    
    unordered_map <int, bool> Table;
    
    for (int j = 0; j < num; j++){
        Table[array[j]] = true;        
    }
    if (Table[100]) {        
        cout << "The Array contains 100" << endl;
    } else {
        cout << "The Array does not contain 100" << endl;        
    }
    if (Table[350]) {
        cout << "The Array contains 350" << endl;   
    } else {
        cout << "The Array does not contain 350" << endl; 
    }
    return 0;
    }
Python:

    array = [200, 400, 100, 50, 350]

    hash_set = set(array)
    
    search_element = 100

    if search_element in hash_set:
      
      print(f"Element {search_element} found in the array")
    else:
      print(f"Element {search_element} not found in the array")

Write a code generate hash value of your name:
  
    #include <iostream>
    #include <string>  
    #include <functional>

    int main()
    {
    std::string name;
    std::cout << "Enter your name: ";
    std::getline(std::cin, name);  
    
    std::hash<std::string> hasher;
        size_t hashValue = hasher(name);
        
        std::cout << "The Hash Value of your name is: " << hashValue << std::endl;

    return 0;
    }

With the help of a figure, explain the problem that occured due to introducing a tombstone to mark the deleted cell.
        
![Hash Tables drawio](https://github.com/user-attachments/assets/8c961b2c-c942-4861-91e5-76463728e1e7)
