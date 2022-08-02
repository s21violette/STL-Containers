# STL-Containers

Here were created following classes: List, Map, Queue, Set, Stack and Vector

List is a sequence container that stores a set of elements with arbitrary size, in the form of nodes connected in sequence by pointers. Each node stores a value corresponding to an element in the list, and a pointer to the next element.

<summary>Specification</summary>
<br />

*List Member type*

This table contains in-class type overrides (typical for the standard STL library) that are adopted to make class code easy to understand:

| Member type            | definition                                                                             |
|------------------------|----------------------------------------------------------------------------------------|
| `value_type`             | `T` defines the type of an element (T is a template parameter)                                  |
| `reference`              | `T &` defines the type of the reference to an element                                                             |
| `const_reference`        | `const T &` defines the type of the constant reference                                         |
| `iterator`               | internal class `ListIterator<T>` defines the type for iterating through the container                                                 |
| `const_iterator`         | internal class `ListConstIterator<T>` defines the constant type for iterating through the container                                           |
| `size_type`              | `size_t` defines the type of the container size (standard type is size_t) |

*List Functions*

This table contains the main public methods for interacting with the class:

| Functions      | Definition                                      |
|----------------|-------------------------------------------------|
| `list()`  | default constructor, creates an empty list                                  |
| `list(size_type n)`  | parameterized constructor, creates the list of size n                                 |
| `list(std::initializer_list<value_type> const &items)`  | initializer list constructor, creates a list initizialized using std::initializer_list<T>    |
| `list(const list &l)`  | copy constructor  |
| `list(list &&l)`  | move constructor  |
| `~list()`  | destructor  |
| `operator=(list &&l)`      | assignment operator overload for moving an object                                |

*List Element access*

This table contains the public methods for accessing the elements of the class:

| Element access | Definition                                      |
|----------------|-------------------------------------------------|
| `const_reference front()`          | access the first element                        |
| `const_reference back()`           | access the last element                         |

*List Iterators*

This table contains the public methods for iterating over class elements (access to iterators):

| Iterators      | Definition                                      |
|----------------|-------------------------------------------------|
| `iterator begin()`    | returns an iterator to the beginning            |
| `iterator end()`        | returns an iterator to the end                  |

*List Capacity*

This table contains the public methods for accessing the container capacity information:

| Capacity       | Definition                                      |
|----------------|-------------------------------------------------|
| `bool empty()`          | checks whether the container is empty           |
| `size_type size()`           | returns the number of elements                  |
| `size_type max_size()`       | returns the maximum possible number of elements |

*List Modifiers*

This table contains the public methods for modifying a container:

| Modifiers      | Definition                                      |
|----------------|-------------------------------------------------|
| `void clear()`          | clears the contents                             |
| `iterator insert(iterator pos, const_reference value)`         | inserts elements into concrete pos and returns the iterator that points to the new element     |
| `void erase(iterator pos)`          | erases an element at pos                                 |
| `void push_back(const_reference value)`      | adds an element to the end                      |
| `void pop_back()`   | removes the last element        |
| `void push_front(const_reference value)`      | adds an element to the head                      |
| `void pop_front()`   | removes the first element        |
| `void swap(list& other)`                   | swaps the contents                                                                     |
| `void merge(list& other)`                   | merges two sorted lists                                                                      |
| `void splice(const_iterator pos, list& other)`                   | transfers elements from list other starting from pos             |
| `void reverse()`                   | reverses the order of the elements              |
| `void unique()`                   | removes consecutive duplicate elements               |
| `void sort()`                   | sorts the elements                |

</details>


| Modifiers      | Definition                                      | Containers |
|----------------|-------------------------------------------------| -------------------------------------------|
| `iterator emplace(const_iterator pos, Args&&... args)`          | inserts new elements into the container directly before `pos`  | List, Vector |
| `void emplace_back(Args&&... args)`          | appends new elements to the end of the container  | List, Vector, Queue |
| `void emplace_front(Args&&... args)`          | appends new elements to the top of the container  | List, Stack |
| `vector<std::pair<iterator,bool>> emplace(Args&&... args)`          | inserts new elements into the container  | Map, Set, Multiset |
