Download Link: https://assignmentchef.com/product/solved-comp9021-lab6
<br>






<h1>1           R Obtaining a sum from a subsequence of digits</h1>

Write a program sum_of_digits.py that prompts the user for two numbers, say available_digits and desired_sum, and outputs the number of ways of selecting digits from available_digits that sum up to desired_sum. For instance, if available_digits is 12234 and sum is 5 then there are 4 solutions:

<ul>

 <li>one solution is obtained by selecting 1 and both occurrences of 2 (1 + 2 + 2 = 5);</li>

 <li>one solution is obtained by selecting 1 and 4 (1 + 4 = 5);</li>

 <li>one solution is obtained by selecting the first occurrence of 2 and 3 (2 + 3 = 5);</li>

 <li>one solution is obtained by selecting the second occurrence of 2 and 3 (2 + 3 = 5).</li>

</ul>

Here is a possible interaction:

<h2>$ python3 sum_of_digits.py</h2>

Input a number that we will use as available digits: 12234

Input a number that represents the desired sum: 5 There are 4 solutions.

<h2>$ python3 sum_of_digits.py</h2>

Input a number that we will use as available digits: 11111

Input a number that represents the desired sum: 5 There is a unique solution.

<h2>$ python3 sum_of_digits.py</h2>

Input a number that we will use as available digits: 11111

Input a number that represents the desired sum: 6 There is no solution.

<h2>$ python3 sum_of_digits.py</h2>

Input a number that we will use as available digits: 1234321

Input a number that represents the desired sum: 5 There are 10 solutions.

<h1>2           R Merging two strings into a third one</h1>

Say that two strings <em>s</em><sub>1 </sub>and <em>s</em><sub>2 </sub>can be merged into a third string <em>s</em><sub>3 </sub>if <em>s</em><sub>3 </sub>is obtained from <em>s</em><sub>1 </sub>by inserting arbitrarily in <em>s</em><sub>1 </sub>the characters in <em>s</em><sub>2</sub>, respecting their order. For instance, the two strings <em>ab </em>and <em>cd </em>can be merged into <em>abcd</em>, or <em>cabd</em>, or <em>cdab</em>, or <em>acbd</em>, or <em>acdb</em>, …, but not into <em>adbc </em>nor into <em>cbda</em>. Write a program merging_strings.py that prompts the user for 3 strings and displays the output as follows:

<ul>

 <li>If no string can be obtained from the other two by merging, then the program outputs that there is no solution.</li>

 <li>Otherwise, the program outputs which of the strings can be obtained from the other two by merging.</li>

</ul>

Here is a possible interaction:

$ python3 merging_strings.py

Please input the first string: ab

Please input the second string: cd

Please input the third string: abcd

The third string can be obtained by merging the other two.

$ python3 merging_strings.py

Please input the first string: ab

Please input the second string: cdab

Please input the third string: cd

The second string can be obtained by merging the other two.

$ python3 merging_strings.py

Please input the first string: abcd

Please input the second string: cd

Please input the third string: ab

The first string can be obtained by merging the other two.

$ python3 merging_strings.py

Please input the first string: ab

Please input the second string: cd

Please input the third string: adcb

No solution

$ python3 merging_strings.py

Please input the first string: aaaaa

Please input the second string: a

Please input the third string: aaaa

The first string can be obtained by merging the other two.

$ python3 merging_strings.py

Please input the first string: aaab

Please input the second string: abcab

Please input the third string: aaabcaabb

The third string can be obtained by merging the other two.

$ python3 merging_strings.py

Please input the first string: ??got

Please input the second string: ?it?go#t##

Please input the third string: it###

The second string can be obtained by merging the other two.

<h1>3           R Longest sequence of consecutive letters</h1>

Write a program longest_sequence.py that prompts the user for a string <em>w </em>of lowercase letters and outputs the longest sequence of consecutive letters that occur in <em>w</em>, but with possibly other letters in between, starting as close as possible to the beginning of <em>w</em>.

Here is a possible interaction:

<h2>$ python3 longest_sequence.py</h2>

Please input a string of lowercase letters: a

The solution is: a

<h2>$ python3 longest_sequence.py</h2>

Please input a string of lowercase letters: abcefgh

The solution is: efgh

<h2>$ python3 longest_sequence.py</h2>

Please input a string of lowercase letters: abcefg

The solution is: abc

<h2>$ python3 longest_sequence.py</h2>

Please input a string of lowercase letters: ablccmdnneofffpg

The solution is: abcdefg

<h2>$ python3 longest_sequence.py</h2>

Please input a string of lowercase letters: abcdiivjwkaalbmmbz

The solution is: ijklm

<h2>$ python3 longest_sequence.py</h2>

Please input a string of lowercase letters: abcpqrstuvwxbcbcddddeffghijklrst

The solution is: abcdefghijkl

<h1>4                    The Gale Shapley algorithm (optional, advanced)</h1>

Read the AMS Feature column on the stable marriage problem and the Gale Shapley algorithm. Write a program gale_shapley.py that

<ul>

 <li>lets the user input the number n of couples,</li>

 <li>either lets the user input names or uses the default names M_1, …, M_n for men and W_1, …, W_n for women,</li>

 <li>either lets the user define preferences or randomly generates preferences.</li>

</ul>

If the preferences have been randomly generated then they are output. Finally, the Gale Shapley algorithm is applied and the matches are displayed.

Here is a possible interaction (the matches are given with women in first position, and lexicographically ordered):

<h2>&gt;&gt;&gt; run_algorithm()</h2>

Enter a strictly positive number for the number of couples: 4

Enter 4 names for the men, all on one line and separated by spaces, or just press Enter for the default “names” M_1, …, M_4:

Enter 4 names for the women, all on one line and separated by spaces, or just press Enter for the default “names” W_1, …, W_4:

Press Enter to get a default preference for all men or women.

Otherwise, input one or more nonspace characters before Enter to be prompted and enter the preferences of your choice:

Preferences for M_1: W_3 W_1 W_4 W_2

Preferences for M_2: W_2 W_1 W_4 W_3

Preferences for M_3: W_2 W_4 W_1 W_3

Preferences for M_4: W_3 W_1 W_2 W_4

Preferences for W_1: M_2 M_3 M_4 M_1

Preferences for W_2: M_4 M_2 M_3 M_1

Preferences for W_3: M_1 M_4 M_3 M_2

Preferences for W_4: M_4 M_1 M_2 M_3

The matches are:

W_1 — M_4

W_2 — M_2

W_3 — M_1

W_4 — M_3

<h2>&gt;&gt;&gt; run_algorithm()</h2>

Enter a strictly positive number for the number of couples: 4

Enter 4 names for the men, all on one line and separated by spaces, or just press Enter for the default “names” M_1, …, M_4:

Enter 4 names for the women, all on one line and separated by spaces, or just press Enter for the default “names” W_1, …, W_4:

Press Enter to get a default preference for all men or women.

Otherwise, input one or more nonspace characters before Enter to be prompted and enter the preferences of your choice: add

List preferences for M_1, in decreasing order: W_1 W_2 W_3 W_4

List preferences for M_2, in decreasing order: W_1 W_4 W_3 W_2

List preferences for M_3, in decreasing order: W_2 W_1 W_3 W_4

List preferences for M_4, in decreasing order: W_4 W_2 W_3 W_1

List preferences for W_1, in decreasing order: M_4 M_3 M_1 M_2

List preferences for W_2, in decreasing order: M_2 M_4 M_1 M_3

List preferences for W_3, in decreasing order: M_4 M_1 M_2 M_3

List preferences for W_4, in decreasing order: M_3 M_2 M_1 M_4

The matches are:

W_1 — M_3

W_2 — M_4

W_3 — M_1

W_4 — M_2

<h1>5                    Sydney temperatures (optional)</h1>

Write a program sydney_temperatures.py that extracts from the file IDCJCM0037_066062.csv, stored in the working directory, the mean min and mean max temperatures for the 12 months of the year for the years 1859 to 2016, and plots them thanks to the matplotlib.pyplot module, which it is convenient to import as plt.

<ul>

 <li>The picture is 5 inches wide and 3.5 inches high—check out figure(), passing as argument the system’s resolution (in dots per inch) for best results. It has as title, with a font size of 10 points, Mean min and max temperatures in Sydney—check out plt.title(). The grid should be displayed—check out plt.grid().</li>

 <li>Denoting by min_temp the largest integer smaller than or equal to the smallest mean min temperature and by max_temp the smallest integer greater than or equal to the largest mean max temperature, the plotting area is a rectangle whose lower left corner has coordinates (0<em>.</em>5<em>,</em>min_temp <em>− </em>1) and whose upper right corner has coordinates (12<em>.</em>5<em>,</em>max_temp + 1)— check out axis().</li>

 <li>The mean min and mean max temperatures for the <em>i</em><sup>th </sup>month, <em>i ∈{</em>1<em>,…,</em>12<em>}</em>, are displayed at points of <em>x</em>-coordinate <em>i</em>, while the averages of the mean min and mean max temperatures for December and January are displayed both at points of <em>x</em>-coordinate 0.5 and at points of <em>x</em>-coordinate 12.5, on blue curves for the mean min temperatures, on red curves for the mean max temperatures—check out plot().</li>

 <li>The area between the curves for the mean min and mean max temperatures is coloured in grey with, to create an appearance of transparency, a value of 0.5 on the alpha channel—check out fill_between().</li>

 <li>The x-axis labels at coordinates 1 to 12 the names of the months of the year, conveniently retrieved from the month_name list of the calendar module, with a font size of 8 points, and displayed slanted—check out xticks() and autofmt_xdate().</li>

 <li>The y-axis labels the temperatures between min_temp and max_temp, in steps of 0<em>.</em>5, with a font size of 4 points—check out yticks().</li>

</ul>

To display the figure, check out plt.show(). Here is the expected output: