🧰 Common Data Structures in Go (Compared to Python)

| Python | Equivalent in Go | Description |
|--------|------------------|-------------|
| list   | slice / array    | Ordered, indexed collection. Slices are dynamic; arrays are fixed size. |
| tuple  | No direct equivalent | Can mimic with fixed-size arrays or structs. Tuples don’t exist in Go. |
| dict   | map[key]value    | Unordered collection of key-value pairs. |
| set    | map[type]bool    | No built-in set, but you can simulate it using a map with bool values. |

🔹 1. slice (like Python list)
```go
var items []int = []int{1, 2, 3}
items = append(items, 4)
fmt.Println(items) // [1 2 3 4]
```
- Dynamic size
- Can be looped through

🔹 2. array (like fixed-size list)
```go
var fixed [3]string = [3]string{"A", "B", "C"}
```
- Fixed size
- Rarely used compared to slices

🔹 3. map (like Python dict)
```go
var ages map[string]int = map[string]int{
    "Alice": 25,
    "Bob":   30,
}
fmt.Println(ages["Alice"]) // 25
```
- Key-value store
- Keys can be strings, ints, etc.

🔹 4. map[type]bool (to simulate a set)
```go
var seen map[string]bool = make(map[string]bool)
seen["apple"] = true
seen["banana"] = true

if seen["apple"] {
    fmt.Println("Already seen apple")
}
```
- Works like a set
- You only check if a key exists

🔹 5. struct (like a simple object or record)
```go
type Person struct {
    Name string
    Age  int
}

var p1 Person = Person{"John", 25}
```
- Combines multiple values into a single custom type
- Like a lightweight class in Python

🧠 Summary

| Go Structure | Description                      | Python Equivalent        |
|--------------|----------------------------------|--------------------------|
| array        | Fixed-size list of same type     | Fixed list               |
| slice        | Dynamic-size list of same type   | list                     |
| map          | Key-value store                  | dict                     |
| map[T]bool   | Emulates a set                   | set                      |
| struct       | Group multiple fields together   | class / record           |

