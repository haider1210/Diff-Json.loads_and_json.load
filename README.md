**Note:** should be string or json-data as josn format then  json.load and json.loads will work properly.
### `json.load()`: For reading JSON from a file.
- **Meaning**: This function reads JSON data directly from a file object (like one opened with `open()`).
- **Use Case**: When you have a JSON file and you want to load its contents into a Python object (like a dictionary or list).

#### Example
```python
import json

# Open the JSON file
with open('data.json', 'r') as file:
    # Load JSON data from the file into a Python object
    data = json.load(file)

print(data)
```
In this example, `data.json` is a file containing JSON data. The `json.load()` function reads this data and converts it into a Python object.

### `json.loads()`: For parsing JSON from a string.
- **Meaning**: This function takes a JSON formatted string and parses it into a Python object.
- **Use Case**: When you have a string containing JSON data (e.g., from a web API response, a database field, or any other source) and you want to convert it into a Python object.

#### Example
```python
import json

# JSON formatted string
json_string = '{"name": "John", "age": 30}'

# Load JSON data from the string into a Python object
data = json.loads(json_string)

print(data)
```
In this example, `json_string` is a string containing JSON data. The `json.loads()` function parses this string and converts it into a Python object.

### Summary
- **`json.load()`**: Reads and parses JSON data from a file.
- **`json.loads()`**: Reads and parses JSON data from a string.

In the context of `json.load()` and `json.loads()`, "parses" means to read and interpret the JSON data, converting it from its raw format (whether it's in a file or a string) into a Python data structure such as a dictionary or a list. 

### Parsing Example

**Before Parsing (Raw JSON Data):**
- **In a file (`data.json`):**
  ```json
  {
    "name": "John",
    "age": 30,
    "city": "New York"
  }
  ```

- **As a string:**
  ```python
  '{"name": "John", "age": 30, "city": "New York"}'
  ```

**After Parsing (Python Data Structure):**
- **Dictionary:**
  ```python
  {
    "name": "John",
    "age": 30,
    "city": "New York"
  }
  ```

### Using `json.load()` and `json.loads()`

- **`json.load()`**:
  ```python
  import json

  with open('data.json', 'r') as file:
      data = json.load(file)  # Parses the JSON data from the file into a Python dictionary

  print(data)  # Output: {'name': 'John', 'age': 30, 'city': 'New York'}
  ```

- **`json.loads()`**:
  ```python
  import json

  json_string = '{"name": "John", "age": 30, "city": "New York"}'
  data = json.loads(json_string)  # Parses the JSON string into a Python dictionary

  print(data)  # Output: {'name': 'John', 'age': 30, 'city': 'New York'}
  ```

### Summary
- **Parsing**: Converting raw JSON data into a usable Python data structure.
- **`json.load()`**: Parses JSON data from a file into a Python object.
- **`json.loads()`**: Parses JSON data from a string into a Python object.
