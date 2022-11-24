# HashTable

This simple package provides a custom implementation of a hash table in Python,
created by following [this tutorial](https://realpython.com/python-hash-table/) written by Bartosz Zaczyński. 
The `HashTable` class replicates many methods from Python dictionaries, including
`HashTable.clear()` and `HashTable.update()`.  

## Installation 

This package is available in [PyPI](https://pypi.org/project/hashtable-nicolerg/1.0.0/). 
Use the package manager [pip](https://pip.pypa.io/en/stable/) to install `HashTable`.

```bash
python3 -m pip install hashtable-nicolerg
```

## Usage 

```python
from hashtable_nicolerg.hashtable import HashTable

# Create an instance of HashTable with initial size 10
# and loading factor threshold 0.5, meaning the HashTable
# will be resized to have 2x capacity whenever the number of 
# key-value pairs is at least half the current capacity
hash_table = HashTable(capacity=10, load_factor_threshold=0.5)

hash_table["blue"] = "sea"              # Add key-value pair "blue":"sea"
hash_table["list"] = [1,2,3]            # Add key-value pair with a mutable value 
len(hash_table)                         # Return number of key-value pairs
hash_table.capacity                     # Return current capacity
hash_table.load_factor                  # Return current load factor
hash_table.keys                         # Return set of keys
hash_table.values                       # Return list of values 
hash_table.pairs                        # Return list of key-value pairs
del hash_table["list"]                  # Delete key-value pair for specified key
hash_table.update({"blue":"0000FF"})    # Update value for key "blue" using a dictionary
hash_table["blue"]                      # Return value for key "blue"
hash_table.clear()                      # Remove all key-value pairs 
```

## Motivation 

Developing this package reinforced knowledge in the following areas:  
* Python classes, including dunder methods  
* Hash table implementation, including handling hash collisions  
* Testing, including TDD, unit tests, and `pytest`  
* Developing Python packages  
