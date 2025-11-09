`DenseMap` is a container that stores values densly (no gaps) in a `std::vector`.
On removal of a value at an arbitrary position (not equal to the last), the last value is swapped in its place to retain contiguous memory usage.
Values can be identified/accessed by a key. The key is persistent across insert and erease.
Internally,`DenseMap` stores key->(vector index)->value relation in an `std::unordered_map`.

This container was inspired by [savas' article about the nomad game engine](https://medium.com/@savas/nomad-game-engine-part-4-1-generic-component-managers-dbe376f10836)
