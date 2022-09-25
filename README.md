# 221_Project


Goals and Overview
In this PA (Programming Assignment) you will:

learn about vectors
learn about pointers
learn about linked lists
learn about management of dynamic memory


Problem Specification
A Linked List is a dynamic linear structure designed to hold any type of data. In this exercise, we develop and use a linked list to manipulate blocks of pixels from an image.

We have broken the image below into 9 Blocks.


orange

Each Block is placed into a Node of a Chain, as shown here:

orange


The Chain can be rearranged, and the image reassembled to create fascinating visual results.

We have provided a starting point for achieving this functionality. It is your task to complete and expand on our implementation.

Specifications for each function you write are contained in the given code. The list of functions here should serve as a checklist for completing the exercise.

In block.cpp
int width() const; Returns the width of the current block.
int height() const; Returns the height of the current block.
void build(PNG & im, int column, int row, int width, int height); From im, grabs the rectangular block of pixels whose upper left corner is at position (column,row), whose width is width, and whose height is height.
void render(PNG & im, int column , int row) const; Draws the current block at position (column,row) in im.
void rotateRight(); This function rotates the block by 90 degrees. Assumes square blocks.
void flipVert(); This function flips the block along its center horizontal axis.
void flipHoriz(); This function flips the block along its center vertical axis.
In chain.cpp
void clear(); Helper function for destructor and assignment operator.
void copy(const Chain & other); Helper function for copy constructor and assignment operator.
~Chain(); Destructor.
void insertBack(const Block & ndata); Insert a new node at the end of the Chain.
void reverse() reverses the order of the nodes in the Chain.
void rotate(int k); for every group of k nodes in the Chain, take the first of that group and move it to the end of the group.
void swap(int i, int j); switch the node in position i with the node in position j.
Implementation Constraints and Advice
We will be grading your work on functionality, efficiency, and memory use. All Chain functionality, aside from the insert and the copy functions, can be achieved by moving existing nodes, rather than by allocating new ones and/or making copies. If you are tempted to use the new function when you are manipulating the Chain, ask yourself if you can achieve your goal by reassigning pointers, instead.

The Chain function is a circular, singly-linked list with a head pointer that points to a sentinel (empty) node. The next pointer of the last node in the chain also points to the sentinel node.

Finally, you'll note that we are asking you to implement special memory management functions for the Chain class. You should ask yourself why we have not made similar requests for the Block class. Why doesn't it need a destructor, copy constructor, or assignment operator?

Getting the Given Code
Download the source files from pa1.zip, and follow the procedures you learned in lab to move them to your home directory on the remote linux machines.

Handing in your code
To facilitate anonymous grading, do not include any personally-identifiable information (like your name, your University ID number, or your cwl) in any of your source files. Instead, before you hand in this assignment, create a file called partners.txt that contains only the CSIDs of people in your collaboration partnership (if one exists), one per line. If you worked alone, include only your own CWL in this file. We will be automatically processing this information, so do not include anything else in the file. (If we must manually correct your submission, you may lose points.) As always, if you're working in a group, each group member must hand in the assignment. (Failure to cite collaborators violates our academic integrity policy.)

The following files are used to grade PA1:

block.cpp
chain.cpp
chain.h
partners.txt
All other files will not be used for grading.

Tests
We have included all of the tests that we will use to grade this PA. If you have no memory leaks and the local tests pass, you will recieve full marks on the PA.
