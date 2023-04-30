Download Link: https://assignmentchef.com/product/solved-cs300-homework-2-bst-and-avl-tree
<br>
In this homework, you are going to implement a phonebook which will help the user to make several operations faster such as searching, adding, deleting contacts. For this purpose, you are required to store the contact information in the <strong>Binary</strong>​<strong> Search Tree (BST) </strong>and​ <strong>AVL</strong>​ tree and experience the implementation and performance differences between both data structures. Your tree implementations <strong>MUST</strong> be template-based.​




<h1>The Contacts Input File</h1>

We will provide you with input files (phonebooks) which are lists of contacts of different sizes where each line is composed of:

<em>firstName lastName phoneNumber</em>​ <em>city</em>​

There is only ONE space between each field. And, each person has only <u>ONE​     </u> first name and last name.

Therefore, in each line, there are exactly 4 strings. An example input file can be as follows:

You can assume that the given input file is valid.




<h1>The functionalities</h1>

There has to be 6 available functions in your program:

<ol>

 <li><em>SearchContact </em></li>

 <li><em>AddContact </em></li>

 <li><em>DeleteContact </em></li>

 <li><em>InOrderPrintToFile </em></li>

 <li><em>PreOrderPrintToFile </em></li>

 <li><em>DrawTreeToFile</em></li>

</ol>

<u>AddContact</u>:​ Adds a new contact for a given firstName, lastName, phoneNumber and city information to both BST and AVL trees. Note that, while inserting into trees, the comparison should be done by alphabetically.

If the given contact info already exists, print a message to warn the user such as “The given contact full name already exists in the database.” To decide whether a contact info already exists, a full match must be done for the full name. Note that full name is the concatenation of firstName and lastName by leaving a blank between them. For instance, if firstName is “Ali” and lastName is “Veli”, then the full name will be “Ali Veli”.




<u>DeleteContact</u>:​ Given the full contact name (firstName+lastName), your program should remove that contact from the phonebook.




<u>SearchAContact</u>:<u>​</u> The search should be performed this way:

<ul>

 <li>Whenever you enter a full name, your program will display the contact(s) that matches the search full name.</li>

 <li>If a partial string is entered, your program should display the contact(s) whose full name starts with the entered partial word (see sample runs for examples).</li>

</ul>




<em><u>InOrderPrintToFile</u></em>​: Print out the phonebook in Pre-order to a file named <em>phonebookInOrder.txt</em>​ ​. The information that should be printed is the full name, phone number and city, the same as the input file but ordered as <em>InOrder</em>​ ​ sorted.

(Debugging hint: the orderings should be identical).




<em><u>PreOrderPrintToFile</u></em>​: Print out the phonebook in Pre-order to a file named <em>phonebookPreOrder.txt</em>​ ​. The information that should be printed is the full name, phone number and city, the same as the input file but ordered as <em>PreOrder</em>​ ​ sorted.




<u>DrawTreeToFile</u>:​ Prints out both BST and AVL (as shown below) into 2 separate files named as <em>phonebookTreeBST.txt</em>​ and <em>phonebookTreeAVL.txt</em>​ ​.



















<h2>The flow of the program</h2>

Once you run your program, it should read the input file (<strong><em>One</em></strong>​<strong><em> of the samples given to you, ex: </em></strong><em>PhoneBook-sample2.txt</em>​) and load all its contacts into a <strong>BST</strong>​ and an <strong>AVL</strong>​ tree. After that, your program should display a menu of functionalities (functions from <strong>1</strong>​ to <strong>5</strong>​ ,​ given in sample runs) that it should perform successfully. Once a selection of a function is made, it should be executed for both trees, the BST and the AVL.




Your program will display the execution times of each operation performed from the list in both trees (The sample runs will explain it thoroughly).




<strong>Important: </strong>Each node in the tree should contain (Full name, Tel number and City).​




Your program should have a list of options to choose which function to run on the phone book, the screenshots below show you how your program should look after running it.

First, it prompts to ask for an input file which is the phonebook <em>.txt</em>​<em> file </em>​that will be provided to you. Then, after entering the <strong>correct</strong>​ file name, the phonebook should be loaded to both, the <strong>BST</strong>​ and​ <strong>AVL</strong>​ trees. (Don’t forget to measure tree creation times for both trees).




From this example, you might have noticed that after loading the phonebook to each tree, it prints the heights of both left and right subtrees for both <strong>BST</strong>​ &amp; ​<strong>AVL</strong> trees to show whether the tree is balanced or not. It is <strong>IMPORTANT</strong>​ to​ note that your program must redisplay the same menu after running any operation in order to perform another one.




<strong>Note:</strong> The InOrder and PreOrder functions should be run using the same choice from the menu (choice number 4).

<h2>Sample runs</h2>

<strong>Input file: </strong><em>PhoneBook-sample(i).txt</em>​         <strong>Output files: </strong><em> </em>

<ul>

 <li><em>txt </em></li>

 <li><em>txt</em></li>

 <li><em>txt </em></li>

 <li><em>txt</em></li>

</ul>

<strong> </strong>

<strong><em><u>Sample Run 1;</u></em></strong><u>​</u> <em>(</em>​ <em>Printing &amp; Drawing)</em><strong>  </strong>

<strong><em>phonebookPreOrder.txt                                                                </em></strong>         <strong><em>phonebookInOrder.txt</em></strong>​

<strong> </strong>

<strong><u>Hint (Drawing): </u></strong>To<u>​</u> draw the tree, you can write a recursive function that traverses the tree’s levels. It is pretty similar to a pre-order printing function with few additional code lines where you have to draw something according to whether you are in the left subtree or right subtree of each node







<h3>Sample Runs 2 &amp; 3</h3>

For Sample runs <strong>2</strong>​ and <strong>3</strong>​ you​ can access their files from the sample runs folder (inside homework2 folder) <a href="https://drive.google.com/drive/folders/14jxCBvUx8gPEjeGn0mhl1MITwJ-dAmRW?usp=sharing">lin</a><u>​ </u><a href="https://drive.google.com/drive/folders/14jxCBvUx8gPEjeGn0mhl1MITwJ-dAmRW?usp=sharing">k</a> since the input sizes are much bigger and there is no room for displaying their outputs in the homework document.







<strong><em><u>Sample Run 4</u></em></strong><u>​</u><em>  (Searching) </em>

<strong>               An example showing the search operation                                         Another example showing the search  </strong>

<strong>                 being faster in an AVL than in a BST tree                                       operation being faster in an AVL than in a  </strong>

<strong>                                                                                                                             BST tree </strong>







<strong>Important:</strong> You should make sure that your code runs on any random input file of any size, therefore, we would probably use other inputs rather than the samples that we have provided you in the homework folder.
















<h3>Sample Run 5​ (​ Deletion)</h3>

As you will notice in the figure below, the deletion in the AVL tree took less time than the deletion in the BST, it is about 500 times faster. However, when the maximum height in the BST is close to the maximum height of the AVL tree, then there will be cases where the deletion in BST is faster than in AVL. Please <strong>note</strong>​ that you should print a message to indicate that the deletion “<strong>terminated</strong>​<strong> successfully</strong>”​ in case the contact to be deleted exists in the phonebook, otherwise, it should print “<strong>Not found</strong>​ ”.​




<h3>Sample Run 6​ (Insertion)</h3>


