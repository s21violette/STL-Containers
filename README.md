# STL-Containers

Here were created following classes: List, Map, Queue, Set, Stack and Vector

### List
List is a sequence container that stores a set of elements with arbitrary size, in the form of nodes connected in sequence by pointers. Each node stores a value corresponding to an element in the list, and a pointer to the next element.

### Map
A map (dictionary) is an associative container that stores key-value pairs sorted in ascending order. It means that each element is associated with some unique key, and its position in the map is determined by its key. Maps come in handy when you want to associate elements with some other value (not an index).
For example, an enterprise is purchasing equipment, and each item has to be purchased more than once. In this case, it is convenient to use a map with a position identifier - purchase volume pair. Here the identifier can be not only a number, but also a string. So, the search is not performed by an index, as in an array, but by an identifier, i.e. a word.

### Queue
Queue is a container with elements organized according to FIFO (First-In, First-Out) principle. Just like a list, an object of the queue container class has pointers to the "tail" and "head" of the queue, but the deletion is performed strictly from the "head", and the addition of new elements is performed strictly in the "tail". It is convenient to think of a queue as a kind of pipe, with elements entering at one end and exiting at another one.

### Set
Set is an associative container of unique elements. This means that the same element can’t be added to a set twice. The set container is associative, because it is also represented as a tree like the map container, and therefore also stores elements in a sorted order.
The difference between a map and a set is that in the set the value itself is unique and not the key as well as the value in the tree is not checked by the key, but by the value itself. There is an appropriate exception when you add an already existing element to a set.

### Stack
Stack is a container with elements organized according to LIFO (Last-In, First-Out) principle. A stack container class object contains pointers to the "head" of the stack; removing and adding elements is done strictly from the "head". You can think of the stack as a glass or a pipe with one sealed end: in order to get to the element placed in the container first, you must take out all the elements on top.

### Vector
Vector is a sequence container that encapsulates a dynamic array for more user-friendly usage. This container does not require manual memory control like standard dynamic arrays, but instead allows any number of elements to be added via `push_back()` and `insert()` methods and, unlike a list, allows any container element to be accessed directly by an index. Elements in a vector are stored sequentially, allowing iterating over the vector not only through the provided iterator, but also by manually shifting the pointer to the vector element. So, a pointer to the first element of a vector can be passed as an argument to any function that expects an ordinary array as an argument. The dynamic resizing of the array does not occur every time an element is added or removed, only when the specified buffer size is exceeded. So, the vector stores two values for a size: the size of the stored array (`size()` method) and the size of the buffer (`capacity()` method).

### Array
Array is a sequence container that encapsulates a static array. You cannot add new elements to an array container, you can only modify the value of the original ones. In terms of interaction, a container array combines the obvious properties of a static array with the main advantage of container classes - a clearer organisation of data. For example, an Array container stores the size of an array and provides iterators. Just like a vector, an array occupies a sequential part of memory and can be passed to a function as a standard array in C. The second template argument of the array class is its actual size.

### Multiset
Multiset is an associative container that follows the logic of a set, but allows identical elements to be stored. This container is different from a list or vector because the elements in the multiset are sorted instantly, just as in a set. But just like a set, a multiset does not allow you to refer to an element by its index, but requires referring to its value, which can be repeated in a multiset.

