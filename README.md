# Puzzling Dancing Links: Seminar in Computational Engineering

## Dependencies

Boost Headers and a recent C++ 17 compiler (tested on g++9 and g++10).

## Building

    g++ --std=c++17 implementation/dancing-links.cpp -o dancing-links -Os -flto -lboost_program_options
    
## Usage

    # Get the help message
    ./dancing-links --help

### Generic XCC Problem Solving

    ./dancing-links --xcc <input-file> [-e] [--mrv]
    
XCC files have the following format, supporting full unicode for items and colors:

    < primary_item_1 primary_item_2 >
    [ secondary_item_1 ]
    primary_item_1 ;
    primary_item_2 ;
    secondary_item_1 : color_1 .
    
Note the `.` at the end of the input, which is the same as in Donald Knuth's
version. To make generating problems easier, this can also be omitted or an `;`
may be used instead.

### Word Puzzles

    ./dancing-links --wordpuzzle <input-file> [-e] [--mrv] [--width <width>] [--height <height>]

Word puzzle files are a line-by-line list of words to arrange in a width x
height grid.
