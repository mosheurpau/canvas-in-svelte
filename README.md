# Create a simple drawing with a combination of lines, rectangles, and circles:

Draw a house with a rectangle as the body, a triangle as the roof, and a rectangle as the door. a sun in the sky using a circle and lines radiating outwards.

# Sun Rays Drawing with HTML5 Canvas and Svelte

The loop runs 8 times, and in each iteration:

- A new path is started.
- The drawing cursor is moved to the center point (400, 50).
- A line is drawn to a point 40 pixels away from the center, at an angle determined by the current iteration of the loop ((i \* Math.PI) / 4). 400 + 40 _ Math.cos((i _ Math.PI) / 4): This calculates the x-coordinate of the endpoint of the ray. 50 + 40 _ Math.sin((i _ Math.PI) / 4): This calculates the y-coordinate of the endpoint of the ray using the sine function, similar to the x-coordinate calculation.
- The line is drawn with the stroke color #FFD700 and a width of 2 pixels.

# Visual Representation

Here's a step-by-step visualization of the rays being drawn:

Iteration 0 (i = 0):

Angle: 0 radians (0 degrees)
Endpoint: (440, 50)
A ray is drawn from (400, 50) to (440, 50).
Iteration 1 (i = 1):

Angle: π/4 radians (45 degrees)
Endpoint: (428.28, 78.28)
A ray is drawn from (400, 50) to (428.28, 78.28).
Iteration 2 (i = 2):

Angle: π/2 radians (90 degrees)
Endpoint: (400, 90)
A ray is drawn from (400, 50) to (400, 90).
Iteration 3 (i = 3):

Angle: 3π/4 radians (135 degrees)
Endpoint: (371.72, 78.28)
A ray is drawn from (400, 50) to (371.72, 78.28).
Iteration 4 (i = 4):

Angle: π radians (180 degrees)
Endpoint: (360, 50)
A ray is drawn from (400, 50) to (360, 50).
Iteration 5 (i = 5):

Angle: 5π/4 radians (225 degrees)
Endpoint: (371.72, 21.72)
A ray is drawn from (400, 50) to (371.72, 21.72).
Iteration 6 (i = 6):

Angle: 3π/2 radians (270 degrees)
Endpoint: (400, 10)
A ray is drawn from (400, 50) to (400, 10).
Iteration 7 (i = 7):

Angle: 7π/4 radians (315 degrees)
Endpoint: (428.28, 21.72)
A ray is drawn from (400, 50) to (428.28, 21.72).
By the end of the loop, 8 evenly spaced rays are drawn around the central point (400, 50).
