# CPE 1040 - Spring 2020

## Criteria for micro:bit JS programs

### 1. General requirements
1. The (README)[README.md] should contain complete grammatically-correct senteces and well-formatted contents. Use the [Github Markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) as a reference.
2. Micro:bit programs should have source file names in all-lower-case dashed strings with the `.js` file extension. For example, `this-is-a-well-formatted-file-name.js`.
3. Each micro:bit program source file should have a short leading comment with:
   1. File name.
   2. Short description of the program.
   3. Name of author.
   4. Date of last modification.
4. All separate tasks should have a short writeup in the [README](README.md) file, containing a link to the corresponding source code file, and, if present, the corresponding demo video.

### 2. Code quality
1. The program should have proper indentation. _Note: The MakeCode environment reformats your code correctly when you press **Download**._
2. Every block of code should contain an inline comment or two, briefly describing its purpose and functionality.	
3. The program should have good structure, with asynchronous (that is, event handlers like `onButtonPress` and `onGesture`) and synchronous (that is, `forever`) code blocks properly differentiated.
4. Variables should be named in either of the following styles:
   1. `variable_name_of_underscore_delimited_lower_case_words`, or
   2. `variableNameInCamelCase`

### 3. JavaScript
1. Variables, including arrays, should be declared with [full static data types](https://makecode.microbit.org/javascript/types).	
2. Programmatic functionality should be encapsulated in [functions](https://makecode.microbit.org/javascript/functions), and, optionally for **bonus** points, [classes](https://makecode.microbit.org/javascript/classes).	
3. Functions in JavaScript are [1st class objects](https://developer.mozilla.org/en-US/docs/Glossary/First-class_Function). All event constructs like `onButtonPressed`, `onGesture`, and `forever` take functions as arguments.	
4. A maximum variety of JS language constructs (loops, conditionals, various operators, encapsulations, event handling, etc) should be used.

### 4. micro:bit			
1. Use of buttons	and/or guestures.
2. Sensible display update.
3. Non-trivial functionality.	
4. Control complexity.
5. Good use of pins for external I/O.

### 5. Videos
1. Each separate task should have an accompanying demo video.
2. Videos should be no longer than 60 seconds.
3. Links to the videos should be embedded in the short task writeups.
