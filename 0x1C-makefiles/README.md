C - Makefiles
In this assignment, I honed my skills in crafting Makefiles.

Tests :heavy_check_mark:
tests: Directory containing test files.
Helper Files :raised_hands:
school.c: C function displaying a seahorse in text, utilized for Makefile practice throughout the project.

main.c: Primary C function executing the functionality defined in school.c.

Header File :file_folder:
m.h: Header file defining the function prototype used in school.c.
Tasks :page_with_curl:
0. make -f 0-Makefile

0-Makefile: Makefile creating an executable school based on
school.c and main.c. Includes:
Rule all for building the executable.
1. make -f 1-Makefile

1-Makefile: Makefile generating an executable school from
school.c and main.c. Extends 0-Makefile
with:
Variable CC defining the compiler.
Variable SRC specifying the .c files to compile.
The all rule only recompiles updated source files.
2. make -f 2-Makefile

2-Makefile: Makefile producing an executable school with
school.c and main.c. Builds on 1-Makefile
with:
Variable OBJ defining the .o files to compile.
Variable NAME setting the executable name.
3. make -f 3-Makefile

3-Makefile: Makefile creating an executable school using
school.c and main.c. Expands on 2-Makefile
with:
Rule clean deleting Emacs/Vim temporary files and the executable.
Rule oclean removing object files.
Rule fclean erasing all temporary files, the executable, and
object files.
Rule re enforcing recompilation of all source files.
Variable RM defining the command to delete files.
4. A complete Makefile

4-Makefile: Makefile creating an executable school with
school.c and main.c. Enhances 3-Makefile
with:
Variable CFLAGS specifying compiler flags -Wall -Werror -Wextra -pedantic.
5. Island Perimeter

5-island_perimeter.py: Python function returning the
perimeter of an island defined in a grid.
Prototype: def island_perimeter(grid):
The parameter grid is a list of lists of integers.
Water is denoted by 0.
Land is represented by 1.
Each element of the lists represents a cell square of side length 1.
Grid cells are connected horizontally/vertically (not diagonally).
The grid is rectangular, with a width and height not exceeding 100.
The grid is entirely surrounded by water, and there is either exactly
one island or none.
The island does not contain lakes (water inside disconnected from
surrounding land).
6. make -f 100-Makefile

100-Makefile: Makefile producing an executable school based on
school.c and main.c. Advances 4-Makefile
by:
Not defining the variable RM.
Never utilizing the string $(CFLAGS).
Refusing to compile if the header m.h is absent.
Functioning even when files with the same names as any of the
Makefile rules exist in the current directory.



