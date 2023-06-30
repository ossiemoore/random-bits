# Overview

Instructions for finding all files with a specfic extension and changing them to another extension.

Applies To: macOS/Linux/UNIX

- Browse to the folder in Finder (macOS) or the filesystem explorer (UNIX/Linux)
- Open the folder in the terminal
  
  <img width="437" alt="change-extension-from-x-to-y-image-1" src="https://github.com/ossiemoore/random-bits/assets/44754148/3085c598-d75a-46f3-be81-92a5108fbba6">
- In the terminal window, run the following command (change `txt` and `tmp` to the extensions you are looking for (`txt`) and what you want to change them to (`tmp`). 
```
find . -type f -name "*.txt" -exec sh -c 'mv "$0" "${0%.txt}.tmp"' {} \;
```

- Close the temrminal
