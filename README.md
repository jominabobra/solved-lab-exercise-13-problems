Download Link: https://assignmentchef.com/product/solved-lab-exercise-13-problems
<br>
<ol>

 <li>Write C++ programs</li>

 <li>Compile C++ programs</li>

 <li>Implement programs that involve method method overriding, and polymorhpism.</li>

</ol>

<h1><a id="user-content-additional-reading" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13#additional-reading" aria-hidden="true"></a>Additional Reading</h1>

This lab exercise requires an understanding of some concepts to solve the problems. You are strongly encouraged to read the following tutorials to help you answer the problems.

<ol>

 <li><a href="https://github.com/ILXL-guides/function-file-organization">Organizing C++ files: function prototypes, implementations, and drivers</a>.</li>

 <li><a href="https://github.com/ILXL-guides/object-parameters-and-return-values">Using objects as parameters and return values in functions</a></li>

 <li><a href="https://github.com/ILXL-guides/arrays-as-parameters">Passing arrays as parameters to functions</a></li>

 <li><a href="https://github.com/ILXL-guides/cpp-file-io">File reading and writing (also includes dealing with arrays)</a></li>

</ol>

<h1><a id="user-content-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13#instructions" aria-hidden="true"></a>Instructions</h1>

Answer the programming problems sequentially (i.e., answer prob01 before prob02). If you have questions let your instructor or the lab assistant know. You can also consult your classmates.

When you answer two programming problems correctly, let your instructor know and wait for further instruction.

<h1><a id="user-content-lab-exercise-guide" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13#lab-exercise-guide" aria-hidden="true"></a>Lab exercise guide</h1>

Here’s a link to the <a href="https://docs.google.com/document/d/1EX01EtrO-pkHNLVPxiq7HNh1f5KnJZnr_dlJcO4T7t0/edit?usp=sharing" rel="nofollow">Lab exercise guide</a> in case you need to review the lab exercise objectives, grading scheme, or evaluation process.

<h1>Driving management software</h1>

You will be creating a base class <code>Car</code> and two derived classes <code>GasolineCar</code> and <code>ElectricCar</code>. The user interface is mostly implemented for you. The focus of this exercise is to demonstrate polymorphism through virtual functions and pointers to derived classes.

<h2><a id="user-content-car-class" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#car-class" aria-hidden="true"></a>Car class</h2>

This class is almost complete so you only need to implement two functions: <code>drive</code> and <code>is_empty</code>. However, here is a rundown of the member functions you will have to use/create.

<h3><a id="user-content-data-members" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#data-members" aria-hidden="true"></a>Data members</h3>

Create a class called <code>Car</code>. It will have the following data members

<ol>

 <li><code>name_</code> which is an <code>std::string</code> that will be the name of the car</li>

 <li><code>year_</code> which is an <code>int</code> that will be the manufacturing year for that car</li>

 <li><code>speed_</code> which is a <code>double</code> that will be the current speed of the car</li>

</ol>

<h3><a id="user-content-member-functions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#member-functions" aria-hidden="true"></a>Member functions</h3>

<h4><a id="user-content-public-methods" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#public-methods" aria-hidden="true"></a>Public Methods</h4>

<h5><a id="user-content-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#default-constructor" aria-hidden="true"></a>default constructor</h5>

<ol>

 <li><code>name_</code> should be initialized to <code>"Steam automobile"</code>.</li>

 <li><code>year_</code> should be initialized to <code>1769</code></li>

 <li><code>speed_</code> should be initialized to <code>0</code></li>

</ol>

<h5><a id="user-content-non-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#non-default-constructor" aria-hidden="true"></a>non default constructor</h5>

The constructor initializes the following variables

For parameters it needs:

<ol>

 <li><code>std::string name</code> for the name of the car.</li>

 <li><code>double year</code> for year if the car.</li>

</ol>

and it initializes the member variables <code>name_</code> and <code>year_</code> with these parameters. additionally, <code>speed_</code> gets initialized to <code>0</code>

<h5><a id="user-content-accessors" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#accessors" aria-hidden="true"></a>accessors</h5>

Create functions that will return each of our data members.

<ol>

 <li><code>std::string name()</code> returns the <code>name_</code> of the car</li>

 <li><code>int year()</code> returns the <code>year_</code> of the car</li>

 <li><code>double speed()</code> returns the <code>speed_</code> of the car</li>

</ol>

<h5><a id="user-content-mutators" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#mutators" aria-hidden="true"></a>mutators</h5>

Create functions that will modify the member variables

<ol>

 <li><code>void set_name()</code> sets the <code>name_</code> of the car</li>

 <li><code>void set_year()</code> sets the <code>year_</code> of the car</li>

</ol>

<h5><a id="user-content-drive" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#drive" aria-hidden="true"></a>drive</h5>

Receives a single <code>double</code> parameter that sets the <code>speed_</code> of the car according to the value provided. <em>This should be a virtual function</em> that derived classes can use/override.

<h5><a id="user-content-is_empty" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#is_empty" aria-hidden="true"></a>is_empty</h5>

Define this as a <em>virtual</em> function that always returns false. It will be overridden in the derived classes.

<h2><a id="user-content-electriccar-class" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#electriccar-class" aria-hidden="true"></a>ElectricCar class</h2>

<h3><a id="user-content-data-members-1" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#data-members-1" aria-hidden="true"></a>Data members</h3>

Create a class called <code>ElectricCar</code>

It will be a class we create that inherits from the <code>Car</code> class. It will have one additional data member

<code>battery_percentage_</code> which is a <code>double</code> that represents the battery percentage.

<h3><a id="user-content-member-functions-1" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#member-functions-1" aria-hidden="true"></a>Member functions</h3>

<h4><a id="user-content-public-methods-1" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#public-methods-1" aria-hidden="true"></a>Public Methods</h4>

<h5><a id="user-content-non-default-constructor-1" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#non-default-constructor-1" aria-hidden="true"></a>non default constructor</h5>

The constructor initializes the following variables

For parameters it needs:

<ol>

 <li><code>std::string name</code> for the name of the car</li>

 <li><code>int year</code> for the year of the car</li>

</ol>

and it initializes the appropriate member variables with these parameters. additionally it sets <code>speed_</code> to <code>0</code>, and sets <code>battery_percentage_</code> to <code>100.0</code>

<h4><a id="user-content-default-constructor-1" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#default-constructor-1" aria-hidden="true"></a>default constructor</h4>

The default constructor should set <code>name_</code> to <code>"Electric carriage"</code>, <code>year_</code> to <code>1832</code>, <code>speed_</code> to <code>0</code> and <code>battery_percentage_</code> to<code>100.0</code>.

<h5><a id="user-content-bool-is_empty" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#bool-is_empty" aria-hidden="true"></a>bool is_empty()</h5>

Returns true if <code>battery_percentage_</code> is 0.

<h5><a id="user-content-drivedouble-speed" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#drivedouble-speed" aria-hidden="true"></a>drive(double speed)</h5>

This override function will perform two steps.

<ol>

 <li>IF the battery percentage is above 0, then it should call <code>drive</code> from the <code>Car</code> object and update <code>battery_percentage_</code>. The value subtracted from the battery percentage is equal to <code>(speed/4)</code>. Specifically, <code>battery_percentage_ -=(speed/4)</code></li>

 <li>IF the remaining <code>battery_percentage_</code> after Step 1 has fallen to or below 0, then call <code>Car</code>‘s drive method to set its speed to 0.</li>

</ol>

<h2><a id="user-content-gasolinecar-class" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#gasolinecar-class" aria-hidden="true"></a>GasolineCar class</h2>

<h3><a id="user-content-data-members-2" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#data-members-2" aria-hidden="true"></a>Data members</h3>

Create a class called <code>GasolineCar</code> It will be a class derived from the <code>Car</code> class and has two additional data members.

<ol>

 <li><code>tank_</code> which is a <code>double</code> that represents the number of gallons a car’s fuel tank can store.</li>

 <li><code>mpg_</code> which is a <code>double</code> that represents the miles per gallon a car can travel.</li>

</ol>

<h3><a id="user-content-member-functions-2" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#member-functions-2" aria-hidden="true"></a>Member functions</h3>

<h4><a id="user-content-public-methods-2" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#public-methods-2" aria-hidden="true"></a>Public Methods</h4>

<h5><a id="user-content-non-default-constructor-2" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#non-default-constructor-2" aria-hidden="true"></a>non default constructor</h5>

The constructor initializes the following variables

For parameters it needs:

<ol>

 <li><code>std::string name</code> for the name of the car</li>

 <li><code>int year</code> for the year of the car</li>

 <li><code>double tank</code> for the amount of fuel this car can store</li>

 <li><code>double mpg</code> for the fuel efficiency for this car.</li>

</ol>

and it initializes the appropriate member variables with these parameters. additionally it sets <code>speed_</code> to 0.

<h4><a id="user-content-default-constructor-2" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#default-constructor-2" aria-hidden="true"></a>default constructor</h4>

The default constructor should set <code>name_</code> to <code>"Gasoline car"</code>, <code>year_</code> to <code>1885</code>, <code>tank_</code> to <code>12</code>, <code>mpg_</code> to 24, and <code>speed_</code> to 0.

<h5><a id="user-content-bool-is_empty-1" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#bool-is_empty-1" aria-hidden="true"></a>bool is_empty()</h5>

Returns true if <code>tank_</code> is 0.

<h5><a id="user-content-void-drivedouble-speed" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#void-drivedouble-speed" aria-hidden="true"></a>void drive(double speed)</h5>

This override function will perform two steps.

<ol>

 <li>IF the amount of fuel left in the <code>tank_</code> is above 0, then it should call <code>drive</code> from the <code>Car</code> object and update <code>tank_</code>. The value subtracted from <code>tank_</code> is equal to <code>(speed/mpg_)</code>. Specifically, <code>tank_ -=(speed/mpg_)</code></li>

 <li>IF the remaining amount in <code>tank_</code> after Step 1 has fallen to or below 0, then call <code>Car</code>‘s drive method to set its speed to 0.</li>

</ol>

<h2><a id="user-content-other-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#other-instructions" aria-hidden="true"></a>Other instructions</h2>

Complete the <code>main</code> function as described. Place your classes in <code>car.hpp</code>. Member functions that take more than five lines or use complex constructs should have their function prototype in <code>car.hpp</code> and implementation in <code>car.cpp</code>.

<h1><a id="user-content-sample-output-1" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#sample-output-1" aria-hidden="true"></a>Sample Output 1</h1>

<pre>Ubiquitous on-board driving management software test: - Gas/battery level sensor -What type of car is being tested?1 - Gasoline Car2 - Electric Car0 - Exit<b>1</b>What is the name of the car? <b>Toyota</b>What year is the car? <b>1996</b>How many gallons of gas can this car store? <b>13</b>How much MPG does this car have? <b>27</b>How fast do you want to drive this car for an hour? <b>50</b>It took Toyota about 8 hour(s) of driving to empty the tank</pre>

<h1><a id="user-content-sample-output2" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#sample-output2" aria-hidden="true"></a>Sample Output2</h1>

<pre>Ubiquitous on-board driving management software test: - Gas/battery level sensor -What type of car is being tested?1 - Gasoline Car2 - Electric Car0 - Exit<b>2</b>What is the name of the car? <b>Tesla</b>What year is the car? <b>2017</b>How fast do you want to drive this car for an hour? <b>60</b>It took Tesla about 7 hour(s) of driving to empty the battery</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob01#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>car.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp car.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Weapons classes</h1>

This program uses four classes: <code>Weapon</code>, <code>Dagger</code>, <code>ShortSword</code>, and <code>Enemy</code>. Implement the classes in <code>weapons.hpp</code> and <code>weapons.cpp</code>.

<h2><a id="user-content-weapon-class" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob02#weapon-class" aria-hidden="true"></a>Weapon class</h2>

Create a <code>Weapon</code> class with the data members <code>int</code> <code>attack_min_</code>, <code>int</code> <code>attack_max_</code>, and <code>std::string</code> <code>name</code>.

Create a default constructor for <code>Weapon</code> that sets the <code>attack_min_</code> to 1, <code>attack_max_</code> to 2, and <code>name_</code> to <code>"weapon"</code>; in that order.

Create a constructor that receives two <code>int</code>s for attack min and max, and an <code>std::string</code> for its name.

Create accessors for all data members.

Create a virtual function <code>attack</code> that returns an <code>int</code> representing the amount of damage done by the weapon. The math for the attack function should be: <code>(random_number % (max - min)) + min</code>

Random numbers can be generated by calling the <code>rand()</code> function that is declared in the <code>random</code> header. That is, you need to <code>#include &lt;random&gt;</code>.

<h2><a id="user-content-daggers-class" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob02#daggers-class" aria-hidden="true"></a>Daggers class</h2>

Create a <code>Daggers</code> class with data members <code>int</code> <code>crit_</code>, and <code>int</code> <code>crit_dice_</code>. Daggers inherit from <code>Weapon</code>.

Create a default constructor for <code>Dagger</code> that will set <code>attack_min_</code> to 2, <code>attack_max_</code> to 3, and the <code>name_</code> to <code>"daggers"</code>. It should also set <code>crit_</code> to 1, and <code>crit_dice_</code> to 18.

Create a constructor that receives two <code>int</code>s for <code>attack_min_</code> and <code>attack_max_</code>, an <code>std::string</code> for the <code>name_</code>, an <code>int</code> for <code>crit_</code>, and an <code>int</code> for <code>crit_dice_</code>. Take note that you can call <code>Weapon</code>s constructor.

Create accessors for all data members.

Unlike the usual <code>Weapon</code> that only computes damage once, daggers can do damage twice and also have a chance to critically damage an enemy. See the details below to get the value returned by <code>attack()</code>.

<strong>Damage 1:</strong>

<ol>

 <li>Compute damage the same way as the <code>Weapon</code>‘s attack function: <code>(random_number % (max - min)) + min</code>.</li>

 <li>Randomly generate a number between 1 and 20. If the number is greater than or equal to <code>crit_dice_</code> then multiply the damage from step 1 by the value of <code>crit_</code>.</li>

</ol>

<strong>Damage 2:</strong>

<ol>

 <li>Compute damage the same way as the <code>weapon</code>‘s attack function: <code>(random_number % (max - min)) + min</code>.</li>

 <li>Randomly generate a number between 1 and 20. If the number is greater than or equal to <code>crit_dice_</code> then multiply the damage from step 1 by the value of <code>crit_</code>.</li>

</ol>

The <code>attack()</code> function should return the sum of damage 1 and damage 2 described above. Take note that damage 1 and damage 2 could produce different values.

<h2><a id="user-content-shortsword-class" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob02#shortsword-class" aria-hidden="true"></a>ShortSword class</h2>

Create a <code>ShortSword</code> class with the data member <code>int</code> <code>multiplier_</code>. <code>ShortSword</code> inherits from <code>Weapon</code>.

Create a default constructor for <code>ShortSword</code> that sets <code>attack_min_</code> to 6, <code>attack_max_</code> to 7, the <code>name_</code> to <code>"shortsword"</code>, and <code>multiplier_</code> to 1.

Create a constructor that receives two <code>int</code>s for <code>attack_min_</code> and <code>atack_max_</code>, an <code>std::string</code> for <code>name_</code> and a <code>int</code> for the <code>multiplier_</code>.

Create accessors for all data members.

Override the <code>attack</code> function to provide a damage multiplier. The steps below describe how to compute the output of the function.

<ol>

 <li>Compute damage the same way as the <code>Weapon</code>‘s attack function: <code>(random_number % (max - min)) + min</code>.</li>

 <li>Randomly generate a number between 1 and the <code>multiplier_</code> (for example, 1 to 4 if the multiplier is 4). The function should return the damage multiplied to the randomly generated number.</li>

</ol>

<h2><a id="user-content-enemy-class" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob02#enemy-class" aria-hidden="true"></a>Enemy class</h2>

Create an <code>Enemy</code> class with two data members, an <code>std::string</code> <code>name_</code>, an <code>int</code> <code>health_</code>.

Create a default constructor for <code>Enemy</code> that sets <code>name_</code> to <code>"dragon"</code> and <code>health_</code> to 500.

Create a constructor that receives an <code>std::string</code> <code>name</code> and <code>int</code> <code>health</code> the assigns it to the data members accordingly.

Create a function called <code>receive_attack</code> that receives a pointer to a <code>Weapon</code> object. Call the <code>Weapon</code> object’s <code>attack</code> function and reduce the <code>Enemy</code>‘s health by that damage, then print out the damage statement: <code>&lt;weapon&gt; dealt &lt;X&gt; damage to &lt;enemy&gt;</code>. If the enemy takes lethal damage, print out: <code>&lt;enemy&gt; has been slain!</code> (replace the values inside &lt; &gt; with the actual values of the object). See the output below to see an actual example.

<h2><a id="user-content-other-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob02#other-instructions" aria-hidden="true"></a>Other instructions</h2>

Complete the <code>main</code> function as described. Place your classes in <code>weapons.hpp</code>. Member functions that take more than five lines or use complex constructs should have their function prototype in <code>weapons.hpp</code> and implementation in <code>weapons.cpp</code>.

<h1><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob02#sample-output" aria-hidden="true"></a>Sample Output:</h1>

<pre>Please enter the name of an enemy: <b>goblin</b>Please enter the enemy's health: <b>10</b>daggers dealt 4 damage to goblinshortsword dealt 6 damage to goblingoblin has been slain!</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob02#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_13/prob02#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>weapons.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp weapons.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<pre><code>make all</code></pre>


