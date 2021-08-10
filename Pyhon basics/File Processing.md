## Read an existing file with Python:
```python3
with open("file.txt") as file:
    content = file.read()
```
- This file is in the same directory as phyton IDE.
- If you use `print(file.read())`: Python will read the very first element and the cursor will go till to end to read the file. But the cursor stays there after the first execution. 
Therefore it makes sense to save it as `content = file.read()`, because then you can print is as many times as you like


## Create a new file with Python and write some text on it:
```python3
with open("file.txt", "w") as file:
    content = file.write("Sample text")
```

## Append text to an existing file without overwriting it:
```python3
with open("file.txt", "a") as file:
    content = file.write("More sample text")
```

## Both append and read a file with:
```python3
with open("file.txt", "a+") as file:
```
