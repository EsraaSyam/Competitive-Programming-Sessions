# STLs

## Outlines

- [STLs](#stls)
  - [session](#Session @ ICPC SCU)
  - [Outlines](#outlines)
  - [Vector](#vector)
  - [Map](#map)
  - [Set](#set)
  - [External links](#external-links)
 
 # Session @ ICPC SCU
 - (part1)[https://cisuezedu.sharepoint.com/sites/ICPC-SCULevel12022/_layouts/15/stream.aspx?id=%2Fsites%2FICPC%2DSCULevel12022%2FShared%20Documents%2FGeneral%2FRecordings%2FSTLs%2D20221023%5F200429%2DMeeting%20Recording%2Emp4&referrer=Teams%2ETEAMS%2DWEB&referrerScenario=teamsSdk%2DopenFilePreview]
 - (part2)[https://cisuezedu.sharepoint.com/sites/ICPC-SCULevel12022/_layouts/15/stream.aspx?id=%2Fsites%2FICPC%2DSCULevel12022%2FShared%20Documents%2FGeneral%2FRecordings%2Fstls%20part%202%2D20221028%5F191444%2DMeeting%20Recording%2Emp4&referrer=Teams%2ETEAMS%2DWEB&referrerScenario=teamsSdk%2DopenFilePreview]
 ---

## Vector

***syntax***

```cpp
//1D vector
vector  <int>  v(sz);
//2D vector
vector  <vector  <int>>  grid(rows);
vector  <vector  <int>>  grid(rows , vector <int> (cols , initial value));
```

***Functions on vectors***

- [begin()](https://www.geeksforgeeks.org/vectorbegin-vectorend-c-stl/) Returns an iterator pointing to the first element in the vector
- [end()](https://www.geeksforgeeks.org/vectorbegin-vectorend-c-stl/)  Returns an iterator pointing to the theoretical element that follows the last element in the vector
- [rbegin()](https://www.geeksforgeeks.org/vector-rbegin-and-rend-function-in-c-stl/) Returns a reverse iterator pointing to the last element in the vector (reverse beginning). It moves from last to first element
- [rend()](https://www.geeksforgeeks.org/vector-rbegin-and-rend-function-in-c-stl/) Returns a reverse iterator pointing to the theoretical element preceding the first element in the vector (considered as reverse end)
- [resize()](https://www.geeksforgeeks.org/vector-chttps://pastebin.com/begin-vector-cend-c-stl/) change the size of the vector without deleting or affecting existing elements
- [assign()](https://www.geeksforgeeks.org/vector-assign-in-c-stl/) erases existing elements and creats a new vector with given size and element
- [emplace()](https://www.geeksforgeeks.org/vector-emplace-function-in-c-stl/), [emplace_back()](https://www.geeksforgeeks.org/vectoremplace_back-c-stl/) ,  [v.insert(position , val)](https://www.geeksforgeeks.org/vector-insert-function-in-c-stl/) ,  [v.push_back()](https://www.geeksforgeeks.org/vectorpush_back-vectorpop_back-c-stl/) Insert a new element.
vector
- [pop_back()](https://www.geeksforgeeks.org/vectorpush_back-vectorpop_back-c-stl/) pop or remove elements from from the back.
- [erase()](https://www.geeksforgeeks.org/vectorclear-vectorerase-c-stl/) remove elements from a container from the specified position or range.
- [clear()](https://www.geeksforgeeks.org/vectorclear-vectorerase-c-stl/) remove all the elements of the vector container
- [swap()](https://www.geeksforgeeks.org/vectorat-vectorswap-c-stl/) swap the contents of one vector with another vector of same type. Sizes may differ.
  
---

***The time complexity for doing various operations on vectors is***

- Random access - constant $O(1)$
- Insertion or removal of elements at the end - constant $O(1)$
- Insertion or removal of elements - linear in the distance to the end of the vector $O(N)$
- Knowing the size - constant $O(1)$
- Resizing the vector - Linear $O(N)$

---

***Articles***

- [GeeksForGeeks](https://www.geeksforgeeks.org/vector-in-cpp-stl/?ref=gcse)
- [cplusplus](https://cplusplus.com/reference/vector/vector/)

---

***Problems**

[Maintain Multiple Sequences](https://atcoder.jp/contests/abc271/tasks/abc271_b)

[Team Olympiad](https://codeforces.com/problemset/problem/490/A)

---

## Map

***syntax**

`// empty map container`

`map < int , int > mp;`

`frequancy map`

```cpp
for(int i = 0 ; i < n ; i++){
    int x;
    cin >> x;
    mp[x]++;
}
// cout map

// the first way
for(auto& [f, s] : mp) 
    cout << f << "  " << s << "\n";

// the second way
for(auto& it : mp)
    cout << it.first << " " << it.second << "\n";

// the third way
for(auto it = mp.begin(); it != mp.end(); it++)
    cout << it -> first << " " << it -> second << "\n";
```

---
  
Maps are [associative containers](https://www.geeksforgeeks.org/containers-cpp-stl/) that store elements in a mapped fashion. Each element has a key value and a mapped value. No two mapped values can have the same key values.

---

***Some basic functions associated with Map***

- [begin()](https://www.geeksforgeeks.org/mapbegin-end-c-stl/) - Returns an iterator to the first element in the map.
- [end()](https://www.geeksforgeeks.org/mapbegin-end-c-stl/) - Returns an iterator to the theoretical element that follows the last element in the map.
- [size()](https://www.geeksforgeeks.org/mapsize-c-stl/) - Returns the number of elements in the map.
- [empty()](https://www.geeksforgeeks.org/mapempty-c-stl/) - Returns whether the map is empty.
- [pair insert(keyvalue, mapvalue)](https://www.geeksforgeeks.org/map-insert-in-c-stl/) - Adds a new element to the map.
- [clear()](https://www.geeksforgeeks.org/mapclear-c-stl/) - Removes all the elements from the map.
- [erase(iterator position)](https://www.geeksforgeeks.org/map-erase-function-in-c-stl/) – Removes the element at the position pointed by the iterator.
- [erase(const g)](https://www.geeksforgeeks.org/map-erase-function-in-c-stl/)– Removes the key-value ‘g’ from the map.
- [map upper_bound()](https://www.geeksforgeeks.org/map-upper_bound-function-in-c-stl/)	Returns an iterator to the first element that is equivalent to mapped value with key-value ‘g’ or definitely will go after the element with key-value ‘g’ in the map
- [map lower_bound()](https://www.geeksforgeeks.org/map-lower_bound-function-in-c-stl/)	Returns an iterator to the first element that is equivalent to the mapped value with key-value ‘g’ or definitely will not go before the element with key-value ‘g’ in the map –> O(log n)


---

***Articles***

[geeksforgeeks](https://www.geeksforgeeks.org/map-associative-containers-the-c-standard-template-library-stl/)

---

***problems***

[Squares and Cubes](https://codeforces.com/contest/1619/problem/B)

[Letter](https://codeforces.com/gym/323462/problem/C)

[Single Number](https://leetcode.com/problems/single-number/)

[Spell Check](https://codeforces.com/contest/1722/problem/A)

[Restaurant Customers](https://vjudge.net/contest/517904#problem/G)

[Everyone is Friends](https://atcoder.jp/contests/abc272/tasks/abc272_b)

[Not a Cheap String](https://codeforces.com/contest/1702/problem/D)

---

## Set

***syntax***

`set < datatype > name;`

defining an empty set

`set < int > val;`

defining a set with values

`set < int > val = {6, 10, 5, 1};`

---

***Properties***

1. **Storing order -** The set stores the elements in **sorted** order.
2. **Values Characteristics** - All the elements in a set have **unique values**.
3. **Values Nature** - The value of the element cannot be modified once it is added to the set, though it is possible to remove and then add the modified value of that element. Thus, the values  are **immutable**.
4. **Search Technique** - Sets follow the **Binary search tree** implementation.
5. **Arranging order -** The values in a set are **un-indexed**.

---

***Some Basic Functions Associated with Set***

- [begin()](https://www.geeksforgeeks.org/setbegin-setend-c-stl/) - Returns an iterator to the first element in the set.
- [end()](https://www.geeksforgeeks.org/setbegin-setend-c-stl/) - Returns an iterator to the theoretical element that follows the last element in the set.
- [size()](https://www.geeksforgeeks.org/setsize-c-stl/) - Returns the number of elements in the set.
- [empty()](https://www.geeksforgeeks.org/setempty-c-stl/) - Returns whether the set is empty.

- [erase(iterator position)](https://www.geeksforgeeks.org/seterase-c-stl/) 	Removes the element at the position pointed by the iterator.

- [count(const g)](https://www.geeksforgeeks.org/set-count-function-in-c-stl/)	Returns 1 or 0 based on whether the element ‘g’ is present in the set or not.

- [lower_bound(const g)](https://www.geeksforgeeks.org/set-lower_bound-function-in-c-stl/)	Returns an iterator to the first element that is equivalent to ‘g’ or definitely will not go before the element ‘g’ in the set.


- [upper_bound(const g)](https://www.geeksforgeeks.org/set-upper_bound-function-in-c-stl/)	Returns an iterator to the first element that will go after the element ‘g’ in the set.

---

***The time complexities for doing various operations on sets are***

- Insertion of Elements - $O(log N)$
- Deletion of Elements - $O(log N)$

---

***problems***

[Remove Duplicates](https://codeforces.com/group/KQlzWufN6x/contest/376252/problem/A)

[Boy or Girl](https://codeforces.com/group/KQlzWufN6x/contest/376252/problem/C)

[Polycarp Writes a String from Memory](https://codeforces.com/contest/1702/problem/B)

---

***Articles***

[geeksforgeeks](https://www.geeksforgeeks.org/set-in-cpp-stl/)

---

## External links

[STL - Playlist (Adel Nassim)](https://www.youtube.com/playlist?list=PLCInYL3l2AainAE4Xq2kdNGDfG0bys2xp)

[STL - Playlist (Cpp Nuts)](https://www.youtube.com/playlist?list=PLk6CEY9XxSIA-xo3HRYC3M0Aitzdut7AA)

