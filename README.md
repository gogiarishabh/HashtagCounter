# Hashtag Counter

A system to find out the n most popular hashtags trending on social media. As the hashtag frequencies are ever changing, there is a need to implement a system that can efficiently support the following operations:
  - Incrementing the frequency of a given hashtag
  - Extracting the most popular hashtag

The following data structures are used for the implementation:
   - Fibonacci Heap: Implement a max priority queue based on the frequencies of the hashtags. (Increase Key runs in O(1) in amortized sense and Remove Max run in O(log n) in amortized sense)
   - Hash Table: A table to keep track of hashtags in the heap, with pointers to the nodes of the Fibonacci Heap.

### Input File
Each line in the input file defines an operation. A line beginning with a “#” represents an insert/increase key operation based on whether the hashtag has been encountered before. A line beginning with a number asks to extract the max n nodes from the Fibonacci heap. A line beginning with the word “stop”, indicates the end of the file. An example input file may contain:

\#saturday 5

\#sunday 3

\#saturday 10

1

\#saturday 12

2

stop

### Output File
The created output file is called “output_file.txt”. Each line in the output file represents a result of an integer query from the input file and displays the top n hashtags as requested separated by commas. An example output file (for previously shown input file) is as follows:create

saturday

saturday,sunday

### Usage

Fire make and execute the program as follows

```sh
$ make
$ ./hashtagcounter sample_input.txt
```
