# cs7638-project-4-mars-glider-solved
**TO GET THIS SOLUTION VISIT:** [CS7638 Project 4-Mars Glider Solved](https://www.ankitcodinghub.com/product/cs-7638-artificial-intelligence-for-robotics-solved-5/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124391&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS7638 Project 4-Mars Glider Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
Mars Glider (Particle Filter) Project

Project Description

The goal of this project is to give you practice implementing a particle filter used to localize a robotic glider that does not have access to terrestrial based GPS satellites. The glider is released from a spacecraft over the surface of mars, and receives a distance to ground measurement from a downward facing radar, as well as an altitude estimate from a barometric pressure sensor.

Your glider has an on-board map of the area it is being dropped into. The map covers an area 10 km on a side (100 sq km), and the robot is supposed to be dropped somewhere near (0,0). The map was generated by radar from the mars surveyor satellite mission, and has a 1×1 meter resolution. Dimensions in the map range from -5,000m to 5,000m.

Your glider will exit the reentry craft somewhere within the mapped area hopefully near (0,0), but possibly as far off as +/- 250m in both X and Y. It will eject out of the reentry craft approximately 5,000 meters (+/- 50m) above “sea level”.

As mars has a thin atmosphere, your glide ratio is 5:1, which means that the glider moves forward 5 meters for every meter it falls. It moves 5m/sec, and falls 1m/s. This means that you have at least 950 seconds to localize the glider before it potentially goes “off-map” and is lost.

You also have at least 4,500 seconds of “glide time” before the glider risks hitting the surface, but would need to steer the glider to keep it within the boundaries of your known map.

Note that the radar sensor [sense function] gives you a (noisy) distance to

“ground”, and not “sea level” (on mars, “sea level” is defined as the mean ground height). The barometric sensor [get_height function] gives you the gliders distance above “sea level”, +/- some Gaussian noise.

The marsglider.py file contains two functions that you must implement, and is the only file you should submit to Canvas-&gt;GradeScope.

Part A

The first function is called estimate_next_pos, and must determine the next location of the glider given its atmospheric height and the radar distance to the ground. If your estimate is less than 5 meters from the target glider’s actual (x,y) position, you will succeed and the test case will end.

Note that each time your function is called, you will receive one additional data point, and it is likely you will need to integrate the information from multiple calls to the function before you will be able to correctly estimate your glider’s position. The “OTHER” variable is passed into your function and can be used to store data which you would like to have returned back to your function the next time it is called (at the gliders next timestep). Note that in part A you are not able to modify the gliders path, so it will be gliding in a (relatively) straight line.

Part B

The second function is called next_angle. The goal of this function is to set the turn angle of the glider (via the rudder) so that the glider returns to the center of its map (0,0) as it glides down to the ground. The test will end once you have navigated the glider to within 10m of the (0,0) target.

Your two functions will have the same input (barometric altitude and RADAR distance to ground), but the next_angle function will return a turning angle in radians (zero for no turn) instead of a predicted location. [Note that the glider can ony turn a set amount per timestep, see the glider.py file for the angle limit.]

The Map Function

Submitting your Assignment

We encourage you to keep any testing code in a separate file that you do not submit. Your code should also NOT display a GUI or Visualization when we import or call your function under test.

Calculating your score

You will receive seven points for each successful test case, even though there are

20 test cases in total (10 in part A, 10 in part B). This means that you only need to successfully complete 15 of the 20 test cases to receive a full score on this assignment. Your maximum score will be capped at 101, although if you are able to solve more than 15 test cases you can brag about it.

Testing Your Code

NOTE: The test cases in this project are subject to change.

We have provided you a sample of 10 test cases where the first five test cases are EASIER than the actual test cases you will be graded with. Each of these first five test cases are designed to allow you to test one aspect of the simulation. Test cases 6-10 are more representative of the test cases that will be used to grade your project.

We have provided a testing suite similar to the one we’ll be using for grading the project, which you can use to ensure your code is working correctly. These testing suites are NOT complete as given to you, and you will need to develop other test cases to fully validate your code. We encourage you to share your test cases (only) with other students on Piazza.

We are using the Canvas-&gt;GradeScope autograder system which allows you to upload and grade your assignment with a remote / online autograder. You must submit your marsglider.py file to Gradescope to receive credit.

We are likely, but not required, to use the last grade you receive, (or your selected grade) via the Canvas-&gt;GradeScope autograder as your final grade at our discretion. (See the “Online Grading” section of the

Syllabus.)

Frequently Asked Questions (F.A.Q.)

Q How can I simplify this problem to make thinking about it easier? A Try solving it in only 2 dimensions, and take a look at the video that inspired the problem: Particle Filter explained without equations https://www.youtube.com/watch?v=aUkBa1zMKv4

Q Are you SURE this can be solved using a particle filter? A Yes. See https://www.youtube.com/watch?v=97Gf392GBNg

Q How exactly are my sources of data related? A Radar gives the glider’s height over ground (+/- measurement error), the barometric measurement height gives the gliders height above sea level (+/- measurement error), and the mapFunction returns the elevation of the ground (above/below sea level) at a specific (x,y) loca-

tion.

Q Radians? How does that work? A The heading of the glider is represented in radians with a range from -pi to pi , with 0 being to the right/east, and -pi being to the left/west (positive pi is ALSO to the left/west).

Q What height is the glider at initially? A The launch vehicle tries to release the glider at 5,000 m, but has a margin of error of +/- 50 meters. Note that your altimeter will give you a better estimate of your height (subject to measurement noise.)
