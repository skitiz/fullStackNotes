## Iterator

If an iterator traverses over a list, it access the items in the same order it was stored in the list.
But for a set, there is no guarantee on the order of the element access.
## Sets

1. Each object in a set is unique.
2. And the order of the objects in the set cannot be guaranteed.

_Set_ inherits from _Collections_ but if the Set is not typed, we can put different data types in the set. Although it is not common.

__Creating a set and element to a set:__
```
Set a = new HashSet();
String element = "element";
a.add(element);
```
_Side Note: Concrete classes in Java are those that have definitions for all the methods present in it. Whereas abstract classes may not have all the methods in the class defined._

_Side side note: Java 8 allows for method definitions in an interface to allow for adding new functionality to existing interfaces in libraries. Its called default interface._


There are four possible implementations to a Set :
1. _java.util.EnumSet_
2. _java.util.HashSet_
3. _java.util.LinkedHashSet_
4. _java.util.TreeSet_

_LinkedHashSet_ guarantees that the order in which elements are inserted into a Set are the same and the order is preserved.

__Iterating Set Elements__
1. Using an `Iterator`.
2. Using a `forEach` loop.

```
Set set = new HashSet();
set.add("123");
set.add("234");
Iterator iterator = set.iterator();

while(iterator.hasNext()) {
        String element = (String) iterator.next();
        System.out.println(element);
}

for (Object object : set) {
        String element = (String) object;
}

Stream stream = set.stream();

stream.forEach((element) -> {System.out.println(element)};);
```
__There is no way to remove objects based on index in a set.__
