# C++ Programming Tips

## Class constructor

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
