# algorithms

## Including

To add this library to your project, simply add those two lines to your *CMakeLists.txt*:
```cmake
add_subdirectory(path/to/algorithms)
target_link_libraries(${PROJECT_NAME} PRIVATE algorithms::algorithms)
```

Then include it as:
```cpp
#include <algorithms/algorithms.hpp>
```

## Documentation

### `translocate()`

Moves an element in a container from its current position to a new one.
The order of the other elements is preserved.<br/>
It takes two iterators, pointing to the current and new locations:

```cpp
auto vec = std::vector<int>{0, 1, 2, 3, 4};

algorithms::translocate(
    vec.begin() + 4,
    vec.begin() + 2
);

// vec is now {0, 1, 4, 2, 3}
```

⚠️ *This currently doesn't work for `std::list`.*