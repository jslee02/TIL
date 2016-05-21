# C++ Programming Tips

## API Design

### Class constructor

#### Overloading constructors with the same prototype

```cpp
// not possible
void resize(int rows);
void resize(int cols);

// one solution using token enum type
enum NoChange_t { NoChange };
void resize(int rows, NoChange);
void resize(NoChange, int cols);
```

## Code Optimization

### STL

* **Q: Which way is better to fill elements into `std::vector`**: 
  * `resize()` + assign
  * `push_back()`
  * `reverse()` + `push_back()`
  * `emplace_back()`
  * `reserve()` + `emplace_back()`
  
* **A: `reserve()` + `emplace_back()`**
 * Rationale: [SO](http://stackoverflow.com/a/32200517/3122234)

--

