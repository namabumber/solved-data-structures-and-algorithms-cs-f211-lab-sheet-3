Download Link: https://assignmentchef.com/product/solved-data-structures-and-algorithms-cs-f211-lab-sheet-3
<br>
<ol>

 <li>You are given two strings <strong><em>t</em></strong> and <strong><em>p</em></strong>. The string <strong><em>t</em></strong> contains all the letters of string <strong><em>p</em></strong> in the same order (it doesn’t have to be contiguous). For example, <strong><em>t</em></strong> could be ‘abdefcb’ and <strong><em>p</em></strong> could be ‘abb’ but <strong><em>p</em></strong> could not be ‘bab’ (order is not preserved) or ‘bxy’ (‘xy’ is not in <strong><em>t</em></strong>). You are also given a set of operations on an array <strong><em>a</em></strong>. Each element <strong><em>a</em></strong>[i] denotes the index of the letter to be removed from string <strong><em>t</em></strong> (<strong>a</strong>[i]&gt;=1). For example, if the array is ‘3 5 4 7 2 1 6’ applied on the string <strong><em>t</em></strong> which is ‘abdefcb’, then first remove the 3<sup>rd</sup> element ‘d’, so <strong><em>t</em></strong> becomes ‘ab<span style="text-decoration: line-through;">d</span>efcb’ (character ‘d’ has been striked through). Then we remove the 5<sup>th</sup> element ‘f’, so <strong><em>t</em></strong> becomes ‘ab<span style="text-decoration: line-through;">d</span>e<span style="text-decoration: line-through;">f</span>cb’(character ‘f’ has been striked through) and so on. Note that after removing one letter, the indices of other letters don’t change. So, if a letter was at 5<sup>th</sup> position and you remove the 3<sup>rd</sup> letter, then still the letter at the 5<sup>th</sup> position stays at 5<sup>th</sup> position.</li>

</ol>

Your task is to determine the maximum number of letters that can be removed from string <strong><em>t</em></strong> following the operations in the array so that string <strong><em>p</em></strong> is obtainable.

Also note that array <strong><em>a</em></strong> has the same size as the string <strong><em>t</em></strong>. So, by the end, after all operations in array <strong><em>a</em></strong> have been executed you should not be left with any unprocessed element in string <strong><em>t</em></strong>, as the elements in array <strong><em>a</em></strong> are all unique. Constraints: |<strong><em>t</em></strong>|≤1000, |<strong><em>p</em></strong>|≤1000.

<strong>Input: </strong>

First line contains string <strong><em>t</em></strong> and second line contains string <strong><em>p</em></strong>.

Third line contains an integer <strong><em>n</em></strong> which denotes the number of elements in array <strong><em>a</em></strong>. The size of <strong><em>a</em></strong> is equal to the size of string <strong><em>t</em></strong>.

Fourth line contains array <strong><em>a</em></strong>.

<strong>Output: </strong>

Print a single integer number, the maximum number of letters that you can remove following the order in array <strong><em>a</em></strong>. <strong>Example :  </strong>abdefcb abb

7

3 5 4 7 2 1 6

<strong>Output :  </strong>

3

<strong>Explanation</strong>:

Following the order of removals in array <strong><em>a</em></strong>, you first remove ‘d’, then ‘f’, then ‘e’. Now if you remove the 7<sup>th</sup> letter which is ‘b’, then abb is in no way obtainable. So, you stop after 3 operations and output is 3.




<ol start="2">

 <li>You are given a string <strong><em>s</em></strong> and <strong><em>m</em></strong> queries. Each of the <strong><em>m</em></strong> queries contains 3 integers f, r, k. Each of the query corresponds to cyclically shifting the values from <strong><em>s</em></strong>[f] to <strong><em>s</em></strong>[r] for k times. One operation of a cyclic shift (rotation) is equivalent to moving the last character to the position of the first character and shifting all other characters one position to the right. Assume index starts from 1. For example, if the string <strong><em>s</em></strong> is ‘abbcde’ and the query is 2, 4, 1, then the values from <strong><em>s</em></strong>[2] to <strong><em>s</em></strong>[4] are ‘bbc’ and shifting it k = 1 times results in ‘cbb’. The final string is ‘acbbde’.</li>

</ol>

<strong> </strong>

<strong>Input: </strong>

The first line contains string <strong><em>s</em></strong> and the second line contains a single integer <strong><em>m</em></strong> denoting the number of queries.

Each of the next <strong><em>m</em></strong> lines contains f, r, k denoting the bounds of each operation. (1 ≤ f ≤ r ≤ |s|≤1000, 1 ≤ k ≤ 1000).

<strong>Ouput: </strong>

A single string which is the result of all the operations. <strong>Example: </strong>abbcde

2

2, 4, 1

1, 3, 2

<strong>Output: </strong>cbabde




<ol start="3">

 <li>Given a singly linked list, write a program to shuffle it according to the following rule: segregate all the elements in such a way that elements at positions k*i (where i starts from 1 and k&lt;=1000, k may not be less than the number of elements present in the linked list, k may not be a multiple of the number of elements present in the linked list) appear before the rest of the elements and the remaining elements are appended in reverse order.</li>

</ol>

<strong>Input: </strong>

The first line contains the value of k.

The second line contains the elements of the linked list (The total number of elements present in the linked list can’t be taken as an input).

<strong>Output: </strong>

An updated linked list based on the segregation rule described in the problem. <strong>Example: </strong>

3

1 2 3 4 5 6 7 8 9

Output:

3 6 9 8 7 5 4 2 1




<ol start="4">

 <li>You are living in a country that has n cities (numbered from 1 to n) connected to each other using n-1</li>

</ol>

bidirectional roads. No city is completely isolated from all the other cities. Each road connects two cities. You love walking and you plan to walk between two cities (u, v), taking the shortest path from u to v.

There are 2 special cities that you dislike visiting namely (x, y). You will avoid all possible paths, in which you first encounter x and then y. The other permutation (first y then x) is allowed. Individual cities x and y appearing separately in the route are fine too. Find out the total number of possible (u, v) pairs such that you do not encounter first the city x then the city y in your route while you are travelling from city u to city v.




<strong>Input:  </strong>

First line contains n, x, y.

Each of the next n-1 lines contains two integers, denoting that these two cities are connected.

<strong>Output:  </strong>

A single integer denoting the total number pairs of cities that follow the restriction. <strong>Example: </strong>

3 1 3

<ul>

 <li>2</li>

 <li>3</li>

</ul>

<strong>Answer: </strong>

5

<strong>Explanation:  </strong>Path 1 (1 to 2), Path 2 (2 to 1), Path 3 (2 to 3), Path 4 (3 to 2) and Path 5 (3 to 2 to 1). The Path (1 to 2 to 3) is not considered because of the restriction.<strong>  </strong>

<strong> </strong>

<ol start="5">

 <li>You are given an N*N matrix filled with 0s and 1s. You have to find out the largest region of 1s in the given matrix. A region is a set of connected 1s. Two 1s are connected if they are adjacent to each other horizontally, vertically, diagonally. <strong>Constraint:</strong> N &lt;= 1000. You have to only print the size of the largest region, i.e., the total number of 1s present in it.</li>

</ol>




<strong>Input: </strong>

First line contains N.

Second line contains elements of the N*N matrix. <strong>Output:</strong> Largest region of 1s <strong>Example:  </strong>

5

0 0 0 0 0

0 1 1 1 0

<ul>

 <li>1 1 0 0</li>

 <li>0 0 0 1</li>

</ul>

0 0 0 0 0 <strong>Output:</strong> 6.




<strong>Explanation:  </strong>

0 0 0 0 0

0 1 1 1 0

<ul>

 <li>1 1 0 0</li>

 <li>0 0 0 1</li>

</ul>

0 0 0 0 0




The red 1s form the largest region. The blue 1 is not a part of the largest region since wrapping around is not considered in any of the directions.




<ol start="6">

 <li>Steph Curry is stuck at the horror house with a string of English lower-case characters as the only weapon. After searching the house, he finds a gate that can only be opened by a string that is an anagram of a palindrome of English lower-case characters. Check if Steph can come out of the horror house or not.</li>

</ol>




<strong>Constraint: </strong>

Length of the string &lt;= 10 <strong>Input: </strong>

Given a string s




<strong>Sample Input 1: </strong>

aabaa

<strong>Sample Output 1: </strong>

Yes

<strong>Sample Input 2: </strong>

abaaa

<strong>Sample Output 2: </strong>

Yes

<strong>Sample Input 3: </strong>a

<strong>Sample Output 3: </strong>

Yes

<strong>Sample Input 4: </strong>

aaba




<strong>Sample Output 4: </strong>

No







<ol start="7">

 <li>Steph fortunately gets out of the horror house using his string. The gate keeper did not like this. He is a big fan of Caesar. He asks you to return the Caesar Cipher of the given password. Caesar Cipher increases the ASCII value of the given letter by 3 and returns the letter corresponding to the new ASCII value. If the ASCII value exceeds the value of z, then start again from the beginning of the lower-case letters.</li>

</ol>




<strong>Constraint: </strong>

Length of the string &lt; 100 <strong>Input Format: </strong>

Given a string s <strong>Sample Input 1: </strong>

abcdefghijklmnopqrstuvwxyz <strong>Sample Output 1: </strong>

defghijklmnopqrstuvwxyzabc <strong>Sample Input 2: </strong>

abaaa

<strong>Sample Output 2: </strong>

deddd

<strong>Sample Input 3: </strong>a

<strong>Sample Output 3: </strong>d

<strong>Sample Input 4: </strong>

aaba

<strong>Sample Output 4: </strong>

dded







<ol start="8">

 <li>The advanced Atlantean city has N buildings. Our superhero Aquaman needs to go from one building in the city to another. The only way Aquaman can move in the city is through a network of M sharks. Every Shark can only move from one building to another. Given a query of the form (x, y), find if Aquaman can reach building y from building x using the network of M sharks. You may be given t such queries. Please note that if a Shark can move from building x to building y that doesn’t imply that it can also move from building y to building x.</li>

</ol>




<strong>Constraint:  </strong>

1 &lt;= N &lt;= 1000 1 &lt;= M &lt;=1000

1 &lt;= t &lt;= 10

1&lt;=x&lt;=N

1&lt;=y&lt;=N <strong>Input: </strong>

The first line contains two integers in the order N, M

Given M lines with two building numbers a, b. Each line i represents that the i<sup>th</sup> shark can move from building a to building b

This line contains value of the number of queries t

Given t lines with two building numbers x, y










<strong>Sample Input: </strong>

5 6

1 4

1 2

1 3

4 2

<ul>

 <li>3</li>

 <li>1</li>

</ul>

3

<ul>

 <li>5</li>

 <li>3</li>

 <li>3</li>

</ul>




<strong>Sample Output: </strong>

No

Yes

Yes




<ol start="9">

 <li>Given a directed graph with N vertices and M edges with no self-loops. Find all the vertices from where all the other vertices can be reached. If no such vertex exists, print the message “no” or else print “yes” and the vertex numbers.</li>

</ol>




<strong>Constraint:  </strong>

1 &lt;= N &lt;= 1000

1 &lt;= M &lt;=1000




<strong>Input: </strong>

The first line contains two integers in the order N, M

Given M lines with two vertex numbers x, y, representing an edge from vertex x to vertex y




<strong>Sample Input: </strong>

5 7

1 2

1 4

1 3

4 2

4 3

3 5

5 1




<strong>Sample Output: </strong>

Yes, 1,3,4,5










****************************