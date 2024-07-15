# <span class="smallcaps">ETH-ZURICH UNIVERSITÀ DELLA SVIZZERA ITALIANA</span>

# FACULTY OF COMPUTER SCIENCE

# Master in Artificial Intelligence

# Topic: Computational Geometry \[2014\] 

Speakers: Heider Jeffer and Prof. Evanthia Papadopoulou

Instructor: Mehdi Jazayeri

Assistant: Sasa Nesic



# Summary

Computational geometry is a branch of computer science devoted to the
study of algorithms which can be stated in terms of geometry. Some
purely geometrical problems arise out of the study of computational
geometric algorithms, and such problems are also considered to be part
of computational geometry.

The main impetus for the development of computational geometry as a
discipline was progress in computer graphics, computer-aided design, and
manufacturing (CAD/CAM), but many problems in computational geometry are
classical.

Other important applications of computational geometry include robotics
(motion planning and visibility problems), geographic information
systems (GIS) (geometrical location and search, route planning),
integrated circuit design (IC geometry design and verification),
computer-aided engineering (CAE) (programming of numerically controlled
(NC) machines). The main branches of computational geometry are:

1.  Combinatorial computational geometry.

2.  Numerical computational geometry.

# Combinatorial computational geometry

The primary goal of research in combinatorial computational geometry is
to develop efficient algorithms and data structures for solving problems
stated in terms of basic geometrical objects: points, line segments,
polygons, polyhedral, etc. Some of these problems seem so simple that
they were not regarded as problems at all until the advent of computers.

# Problem classes

The core problems in computational geometry may be classified in
different ways, according to various criteria. The following general
classes may be distinguished.

# Static problems

In the problems of this category, some input is given and the
corresponding out- put needs to be constructed or found.

# Geometric query problems

In geometric query problems, commonly known as geometric search
problems, the input consists of two parts: the search space part and the
query part, which varies over the problem instances. The search space
typically needs to be preprocessed, in a way that multiple queries can
be answered efficiently.

# Dynamic problems

Yet another major class is dynamic problems, in which the goal is to
find an efficient algorithm for finding a solution repeatedly after each
incremental modification of the input data (addition or deletion of
input geometric elements). Algorithms for problems of this type
typically involve dynamic data structures.

# Variations

Some problems may be treated as belonging to either of the categories,
depending on the context. For example, consider the following problem.

# Numerical computational geometry

This branch is also known as geometric modeling and computer-aided
geometric design (CAGD). Core problems are curve and surface modeling
and representation. The most important instruments here are parametric
curves and parametric surfaces, such as Bezier curves, spline curves,
and surfaces. An important non-parametric approach is a level set
method. Application areas include shipbuilding, aircraft, and automotive
industries.


### Example
This example demonstrates a practical implementation of a classic problem in combinatorial computational geometry. Computational geometry involves designing efficient algorithms and data structures to solve geometric problems, such as finding intersections, convex hulls, or nearest neighbors, which are crucial in various applications from computer graphics to robotics and CAD/CAM. Each problem type typically requires tailored algorithms and approaches suited to its characteristics and constraints.


To provide a comprehensive implementation example in Python for each section of your research paper on Computational Geometry, let's focus on a specific problem and demonstrate its solution. We'll choose a classic problem from combinatorial computational geometry: **finding the closest pair of points** in a set of 2D points.

### Implementation in Python

```python
import math

# Function to calculate the Euclidean distance between two points
def euclidean_distance(p1, p2):
    return math.sqrt((p1[0] - p2[0]) ** 2 + (p1[1] - p2[1]) ** 2)

# Brute-force approach to find the closest pair of points
def brute_force_closest_pair(points):
    min_distance = float('inf')
    closest_pair = None

    n = len(points)
    for i in range(n):
        for j in range(i + 1, n):
            distance = euclidean_distance(points[i], points[j])
            if distance < min_distance:
                min_distance = distance
                closest_pair = (points[i], points[j])

    return closest_pair, min_distance

# Example usage:
if __name__ == "__main__":
    points = [(1, 1), (5, 5), (3, 3), (12, 30), (40, 50), (5, 1), (12, 10), (3, 4)]
    
    closest_pair, min_distance = brute_force_closest_pair(points)
    print("Closest pair:", closest_pair)
    print("Distance:", min_distance)
```

### Explanation

1. **Euclidean Distance Calculation**: The `euclidean_distance` function computes the distance between two points in 2D space using the Euclidean distance formula.

2. **Brute-force Closest Pair Algorithm**: The `brute_force_closest_pair` function implements a simple O(n^2) brute-force algorithm to find the closest pair of points in a given list `points`. It iterates through all pairs of points, computes their distances, and keeps track of the minimum distance encountered.

3. **Example Usage**: In the example usage section, we create a list of 2D points `points` and apply the `brute_force_closest_pair` function to find the closest pair of points and their distance.
