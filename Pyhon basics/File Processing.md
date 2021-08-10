## Read an existing file with Python:
```python3
with open("file.txt") as file:
    content = file.read()
```
- If you only want reading right use `open("file.txt", "r")`
- This file is in the same directory as phyton IDE. You need to specify the path if not.
- If you use `print(file.read())`: Python will read the very first element and the cursor will go till to end to read the file. But the cursor stays there after the first execution. 
Therefore it makes sense to save it as a string `content = file.read()`, because then you can print is as many times as you like

## Close an existing file with Python:
```python3
    file.close()
```
- normaly you don't need to close the file when using it with the `with open("file.txt") as file` methode. It closes automaticly.

## Write in a file with Python:
- You will overwrite the old text by using:
```python3
with open("file.txt", "w") as file:
    content = file.write("Sample text")
```

## Create a new file with Python and write some text on it:
```python3
with open("new_file.txt", "w") as file:
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
