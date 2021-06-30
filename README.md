# MAP COLORING USING BACKTRACKING

## Introduction

 Figuring out what color to put where while making a map can be a task if it has to be done by hand. Map coloring using backtracking is an extremely useful application that has been used widely since the late 1970’s. It is one of the early applications of artificial intelligence. It is solved by the constraint satisfaction problem which efficiently colors the map making sure that there are no two adjacent regions have the same color.

## Pseudocode

The primary algorithm of our pseudocode is the backtracking algorithm.
The pseudocode works as follows:

    • Detect the different region borders of the map by finding the pixels that are on the borders
    • Discard the unwanted pixels i.e. the pixels that are outside the map and the white background.
    • Find all pixels in each region by selecting any one pixel and checking its neighbors. 
    • If the neighbors have the same color as the selected pixel, the neighbors are also in the same region. If not, the neighbors are in another region.
    • We convert the map into a graph and detect its nodes
    • For coloring the map, we start with any random color in a region and keep filling its neighbors.
    • We keep running the algorithm until we finish coloring the map or there comes a point where we cannot correctly implement the algorithm i.e. it is not possible for two neighboring regions to have different colors, at which point, we will start with another initial state.


## Data Format and Cleaning

The format of our input is a .png file which will be a blank image of a map. The borders of the map should be in white for the code to work correctly.
We will take this image and use OpenCV library to read the image. We detect the whitespace in the image so that we can ignore those parts. We specify 4 colors that will be used to color the map. These colors can be changed according to our will. The final output will also be an image which has the map colored correctly so that no two neighboring regions have the same color. For better readability, chose 4 colors that are distinct from each other.

 Time Complexity and Space Complexity
 Time complexity of the algorithm is the time complexity of backtracking algorithm which is O(m^V) where m is the number of different colors and V is the vertices of our graph. Space complexity of the algorithm is O(V).


## Input Image

![Picture1](https://user-images.githubusercontent.com/79534543/123884246-d28f9600-d918-11eb-9c95-8e2469df2b34.jpg)

## Output Image

![Picture2](https://user-images.githubusercontent.com/79534543/123884312-f6eb7280-d918-11eb-998b-3bc155c5eb73.jpg)

## Conclusion and Future scope

We have implemented the backtracking algorithm correctly which helps us in coloring the map. This algorithm is better than brute force, but it still takes quite some time to run and in the future we could probably come up with an algorithm that doesn’t take exponential time. We could also give all the options for the output in the form of a .gif file instead of giving just one single output.

To run our application run the following from command line(from the project's directory):

	python main.py map1.png

Also verify that all the python libraries and Python3 is installed on the system.

The code runs for both jpeg and png images

One caveat for the images is to have white border for separating the different regions.	

## Project by

	-Kavit Shah
	-Dhaivat Patel
	-Monaal Sanghvi
