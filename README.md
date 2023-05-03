Download Link: https://assignmentchef.com/product/solved-cs102-assignment1-tennis-player-main
<br>
To complete this assignment, you need knowledge of the material covered in CS-101, as well as knowledge of the ADT list covered at the beginning of CS-102. The goal is to design and implement a simple database system to store tennis players and tennis matches and some statistics.

I N P U T F I L E F O R M AT

<table>

 <tbody>

  <tr>

   <td width="389"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

Your program will accept 1 argument in the command line: a file name. This file should be in the current directory, and it should contain the input data for the tennis database (see below).

<em>Tennis Player Line. </em>

Each tennis player is represented by this info separated by <strong>/</strong> and in this order:

<ul>

 <li>The word <strong>PLAYER</strong>, a token indicating that this line represents a tennis player.</li>

 <li>An alphanumeric sequence representing the unique id of the player (e.g. <strong>FED81</strong>, <strong>DJO87</strong>).</li>

 <li>A word representing the first name of the player (e.g. <strong>ROGER</strong>, <strong>NOVAK</strong>, <strong>RAFAEL</strong>).</li>

 <li>A word representing the last name of the player (e.g. <strong>FEDERER</strong>, <strong>DJOKOVIC</strong>, <strong>NADAL</strong>).</li>

 <li>A number representing the year the player was born (e.g. <strong>1981</strong>, <strong>1987</strong>, <strong>1986</strong>).</li>

 <li>A word representing the country of the player (e.g. <strong>SWITZERLAND</strong>, <strong>SERBIA</strong>, <strong>SPAIN</strong>).</li>

</ul>

This is an example of a player line: <strong>PLAYER/FED81/ROGER/FEDERER/1981/SWITZERLAND</strong>

<em>Tennis Match Line. </em>

Only single matches are allowed, each represented by this info separated by <strong>/</strong> and in this order: <sup>1</sup>

<ul>

 <li>The word <strong>MATCH</strong>, a token indicating that this line represents a tennis single match.</li>

 <li>An alphanumeric sequence representing the <em>id</em> of the <em>first player</em> of the match (e.g. <strong>FED81</strong>). 3 An alphanumeric sequence representing the <em>id</em> of the <em>second player</em> of the match (e.g. <strong>NAD86</strong>). <sup>2</sup></li>

 <li>An 8-digit numeric sequence representing the match date, in the format YYYYMMDD.</li>

 <li>A word representing the location (i.e. the tournament) of the match (e.g. <strong>WIMBLEDON</strong>).</li>

 <li>An alphanumeric sequence representing the match score (e.g. <strong>6-4,2-6,7-6</strong>).</li>

</ul>

This is an example of a match line: <strong>MATCH/NAD86/DJO87/20150101/ROME/6-2,6-3,6-4 </strong>

<em>Input File Example. </em>

The following is an example of the content of the data file which could be read by this program:

<strong>PLAYER/FED81/ROGER/FEDERER/1981/SWITZERLAND </strong>

<table>

 <tbody>

  <tr>

   <td width="389"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<strong>PLAYER/DJO87/NOVAK/DJOKOVIC/1987/SERBIA </strong>

<strong>PLAYER/NAD86/RAFAEL/NADAL/1986/SPAIN </strong>

<strong>MATCH/FED81/NAD86/20070308/WIMBLEDON/6-4,2-6,7-6 </strong>

<strong>MATCH/DJO87/FED81/20121231/US OPEN/6-2,3-6,6-7,7-5,6-1 </strong>

<strong>MATCH/NAD86/DJO87/20150101/ROME/6-2,6-3,6-4 </strong>

<strong>Note:</strong>  The correct file format lists all the players before any match. Any input file violating this requirement should be discarded, and an appropriate error message should be displayed. <strong>Note:</strong>  All the strings should be stored internally and processed in uppercase.

<strong>Note:</strong>  Input from the console and from files should be handled using the Java <strong>Scanner</strong> class. <sup>3</sup>

Your program will begin by reading in this information from the input file, and then storing it in the tennis database using the appropriate format.




<h1>F U N C T I O NA L I T Y</h1>

Once started, and the input file loaded successfully, your program will then interact with the user through the console, by offering the following commands:

<ul>

 <li><em>Print All Players. </em></li>

</ul>

Print the list of players, sorted alphabetically by their ids. The program should print all players in the database in an appropriate format (see example), including the win/loss record for each player. The same sorted order (sorted alphabetically by player id) should be used to store the data.

<ul>

 <li><em>Print Matches of a Player. </em></li>

</ul>

Print all matches of the input player, sorted by date (most recent first). The program asks the user for a player id, and then prints all matches including that id as the first or second player.

If input id cannot be found in the database, an appropriate error message should be displayed. The same sorted order (sorted by date, most recent first) should be used to store the data.

<ul>

 <li><em>Print All Matches. </em></li>

</ul>

<table>

 <tbody>

  <tr>

   <td width="389"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

Print all matches, sorted by date (most recent first). The program should print the match details including the full name of each player (instead of their ids).

The same sorted order (sorted by date, most recent first) should be used to store the data.

<ul>

 <li><em>Insert New Player. </em></li>

</ul>

Insert a new player. The program should prompt the user to input the appropriate information on the console, and add the specified data to the database.

If the input player has an id already stored in the database (duplicate id), the player should be rejected, and an appropriate error message should be displayed.

<ul>

 <li><em>Insert New Match. </em></li>

</ul>

Insert a new match. The program should prompt the user to input the appropriate information on the console, and add the specified data to the tennis database.

Only matches with both players in the database should be stored internally, all the other matches should be considered invalid and discarded, and an appropriate error message should be displayed.

<ul>

 <li></li>

</ul>

Exit the program. The program should terminate.

<h1>C O N S O L E S E S S IO N E X A M P L E</h1>

The following is an example of a console interactive session:

<strong>CS-102 Tennis Manager – Available commands: </strong>

<ul>

 <li><strong>–&gt; Print All Players </strong></li>

 <li><strong>–&gt; Print All Matches of a Player </strong></li>

</ul>

<strong>… </strong>

<strong>6 –&gt; Exit </strong>

<strong>Your Choice? 1 </strong>

<strong> </strong>

<table width="44">

 <tbody>

  <tr>

   <td width="44"><strong>DJO87</strong><strong>FED81</strong><strong>NAD86</strong></td>

  </tr>

 </tbody>

</table>

<strong>: NOVAK DJOKOVIC, 1987, SERBIA, 214/34 </strong>

<strong>: ROGER FEDERER, 1981, SWITZERLAND, 285/47 </strong>

<strong>: RAFAEL NADAL, 1986, SPAIN, 195/27 </strong>

<strong> </strong>

<strong>CS-102 Tennis Manager – Available commands: </strong>

<ul>

 <li><strong>–&gt; Print All Players </strong></li>

 <li><strong>–&gt; Print All Matches of a Player </strong></li>

</ul>

<strong>… </strong>

<strong>6 –&gt; Exit </strong>

<strong>Your Choice? 2 </strong>

<table>

 <tbody>

  <tr>

   <td width="388"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<strong>Enter Player ID: DJO87 </strong>

<strong> </strong>

<table width="297">

 <tbody>

  <tr>

   <td rowspan="2" width="88"><strong>2015/01/01</strong><strong>2012/12/31</strong></td>

   <td rowspan="2" width="17"><strong>, </strong><strong>, </strong></td>

   <td width="175"><strong>R.NADAL – N.DJOKOVIC</strong></td>

   <td width="17"> </td>

  </tr>

  <tr>

   <td colspan="2" width="192"><strong>N.DJOKOVIC – R.FEDERER</strong></td>

  </tr>

 </tbody>

</table>

<strong>, ROME, 6-2,6-3,6-4 </strong>

<strong>, US OPEN, 6-2,3-6,6-7,7-5,6-1 </strong>

<strong>Note:</strong>  Remember to include in your prints the win-loss record (print players) and the player full name (print matches), as well as the required sorting for each print.

<strong>Note:</strong>  This is just an example; your console menu may operate/appear differently.

<strong>Note:</strong>  You should create/test different input files to make sure your program is correct and robust. Do not assume that testing the program on one input file is sufficient.

<h1>I N T E R NA L R E Q U I R E M E N T S</h1>

Your program should be designed with modularity and modifiability in mind, also because you will be revising and extending this program in the next assignment.




The following are the requirements for the classes and ADTs that you will need to design and code.

<em>Class TennisPlayer. </em>

Define a class <strong>TennisPlayer</strong> to implement the <strong>TennisPlayerInterface</strong>.

The <strong>TennisPlayer</strong> class contains members corresponding to a given player, and methods to deal with the player statistics (e.g. win/loss record).

<em>Class TennisMatch. </em>

Define a class <strong>TennisMatch</strong> to implement the <strong>TennisMatchInterface</strong>.

The <strong>TennisMatch</strong> class contains members corresponding to a given match, and methods to deal with the match details (e.g. winner).

This class should include an internal recursive function to parse the score (recursively on the sequence of set scores) in order to identify the winner (stored internally).

<em>Class TennisDatabase. </em>

<table>

 <tbody>

  <tr>

   <td width="389"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

Define a class <strong>TennisDatabase</strong> to implement the <strong>TennisDatabaseInterface</strong>.

The <strong>TennisDatabase</strong> class contains methods which allow to manipulate a collection of tennis records and, for this assignment, this class should be designed to store 2 objects:

<ul>

 <li>An object of type <strong>TennisPlayerContainer</strong>, storing all players.</li>

 <li>An object of type <strong>TennisMatchContainer</strong>, storing all matches.</li>

</ul>

<em>Class TennisPlayerContainer. </em>

The <strong>TennisPlayerContainer</strong> class implements the <strong>TennisPlayerContainerInterface</strong>. The <strong>TennisPlayerContainer</strong> class should be a two-level list to store tennis players:

<ul>

 <li>The upper-level list will be a circular doubly linked list (without dummy head nodes<em>)</em>, called <strong>TennisPlayerContainer</strong> and sorted by player id (alphabetically). The nodes in the upper-level linked list will be instances of the <strong>TennisPlayerContainerNode</strong> class, and they will store tennis players, with one node per player.</li>

 <li>Each <strong>TennisPlayerContainerNode</strong> object will also contain a lower-level linked list: a sorted linked list implemented by the class <strong>SortedLinkedList&lt;TennisMatch&gt;</strong>, and storing the tennis matches of that player, sorted by date (most recent first). <sup>4</sup> <sup>5</sup></li>

</ul>




<ul>

 <li>You should define a generic class <strong>SortedLinkedList&lt;T&gt;</strong> implementing a sorted linked list: using the type parameter <strong>T</strong> to customize the type of the data stored in the list; and constraining <strong>T</strong> to represent a <em>“comparable”</em> type (see bounded type parameters and wildcards). <sup>6</sup> <sup>7</sup> <sup>8</sup></li>

</ul>

For its implementation, the class <strong>SortedLinkedList</strong> will require a supporting generic class <strong>SortedLinkedListNode&lt;T&gt;</strong> to store the data and the link required for its implementation.

<em>Class TennisMatchContainer. </em>

The <strong>TennisMatchContainer</strong> class implements the <strong>TennisMatchContainerInterface</strong>.

The <strong>TennisMatchContainer</strong> class should be a dynamically allocated array-based list to store tennis matches, sorted by date (most recent first). This list/container should be implemented using an array of <strong>TennisMatch</strong> objects, re-allocating the array (i.e. increasing its physical size) whenever you need to add a new tennis match and the array is full. <sup>9</sup>

<em>Class Assignment1. </em>

You should define a class <strong>Assignment1</strong> with a <strong>main</strong> method which uses a <strong>TennisDatabase</strong> object to store data and perform the operations requested by the user.

<table>

 <tbody>

  <tr>

   <td width="388"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

Additionally, this is the only class allowed to print-to and read-from the console.

<em>Package TennisDatabase. </em>

All the classes mentioned above, except <strong>Assignment1</strong>, should be part of the <strong>TennisDatabase</strong> package, and the only <strong>public</strong> classes/interfaces in this package should be: <strong>TennisDatabase</strong>, <strong>TennisPlayer</strong>, <strong>TennisMatch</strong>, their associated interfaces, and all the exception classes.

<strong>Note:</strong>  All the interfaces and exception classes and generic classes will be discussed in-class and provided by the instructor right after the beginning of this assignment.

<em>Coding Style. </em>

As always, your program should use good coding style, that will be evaluated accordingly to standard guidelines. <sup>10</sup>




<em>Exception Handling. </em>

Your program should integrate standard exception handling: catch and properly handle all exceptions generated by any system routines you use, as well as any exceptions your own code generates (that is, your <strong>main</strong> method should not throw any exception).




<h1>E VA LUAT IO N F O R M</h1>




S T U D E N T NA M E :

<strong>       </strong>

<table width="624">

 <tbody>

  <tr>

   <td width="528">FUNCTIONALITY AND INTERNAL REQUIREMENTS Input file loaded (5)Print tennis players (5)Prints tennis matches (5)Prints matches of player (5)Insert new player (5)Insert new match (5) TennisPlayer class (5)TennisMatch class (5)TennisDatabase class (5)TennisPlayerContainer class (10)TennisMatchContainer class (10)Assignment1 class (5)</td>

   <td width="41"> </td>

   <td width="55">___ / 70</td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="389"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>




<table width="624">

 <tbody>

  <tr>

   <td width="528">D E S IG N A N D S T Y L E A N D SU B M I S S IO N OOP principles and design (10) Compilation and exception handling (10) Coding style and commenting (10) Submission and delay (…)</td>

   <td width="41"> </td>

   <td width="55">___ / 30</td>

  </tr>

 </tbody>

</table>




<table width="624">

 <tbody>

  <tr>

   <td width="101">T O TA L</td>

   <td width="120"> </td>

   <td width="41"> </td>

   <td width="266"> </td>

   <td width="41"> </td>

   <td width="55">___ / 100</td>

  </tr>

 </tbody>

</table>


