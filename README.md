# StokeAggregation
## Group members:
* Montana Fowler
* Ben Gabinet
* Leon Lei
* Fangrui Tong

## Project Summary: 
We are planning to implement a stroke aggregator using C++ with Blend2d. We plan to segment work as follows:

### Week 1: 
Planning, test cases, firm grasp of paper. Set up version control. We will start by having one person setting up our vector graphics library. At the same, one of us will be writing a single metric for stroke clustering, while the rest work on setting up data structures to store vector drawings & metrics. (Ben: Graphics Lib, Leon: Metrics (likely angular compatibility since this is used for clustering), Montana/Fawn: data structures, Montana: produce test drawings on tablet)
### Week 2: 
Once we have some basic metrics down, we will work on basic cluster formation and fitting clusters to a single stroke. We will focus on getting metrics working will a very basic test image. (Once displaying images is done, we will split into teams of two: one for metrics and one for clustering, Ben/Montana: Metrics, Leon/Fawn: Clustering) Intended deliverables: Correct clustering for obvious test cases (not necessarily visual, just the correct number of clusters).
### Week 3: 
Work on combining metrics will begin here, as well as testing on more complex images and metrics. Ben will work on displaying our images Deliverables: Correct outputs with more complex test images, using combined metrics. Potentially display our final images.
### Week 4: 
Work on fine grained clustering and continue working on displaying images. At this point we will hopefully be working on fixing any bugs.
### Week 5: 
Grace period!

## Member Backgrounds:
### Ben Gabinet: 
3D Animation student and 2D Game Engines TA. Programming for Maya, Nuke, Houdini, and After Effects. Experience in web development and software engineering. Knowledgeable in 2D vector design programs such as premier.

I would like to learn more about vector graphics and programming for software that works in 2D.
### Leon Lei: 
Artificial Intelligence/Machine Learning, Graphics, Computer Vision, Web Apps (HTML, SVG, visualization), SWE, Basic (and not as basic) Maths.

I would be interested in learning more about how they cluster and refine clusters, as well as gain more comfort with optimization problems
### Montana Fowler:
Graphics TA, Software Engineering Experience, drawing pad, some vectorized drawing experience, artist, stats, linear, research in visual computing lab

What I would like to learn: what its like to build a support artist tool, how to read strokes and artistic intention through programming, how to implement a research paper, use Blend2d api, optimization
### Fawn Tong: 
Computer Vision, Software Engineering, Web Development (HTML, CSS, SVG, web apps TA), experience in implementing vectorized drawing apps, experience in 2d drawing/sketching, research in graphics lab

What I would like to learn: Solving for optimization problems, creating a 2d drawing app with an integrated backend. 

## Paper: 
https://www.cs.ubc.ca/labs/imager/tr/2018/StrokeAggregator/StrokeAggregator_authorversion.pdf

## Necessary Libraries/Resources:
* https://blend2d.com/
* Version Control
* Solver for Optimization
* Math help slides/papers 

## Metrics:
* Angular compatibility -> main metric for clustering
* Connectedness -> strokes are connected (like multiple connected strokes to make a curve), used to generate initial clusters
* Narrowness -> used for cluster refinement (branch separation), ratios of width and length to determine lines vs. rectangles
* Strength in numbers -> repeated strokes in same area, includes outlier case when artist tries to cover a mistake
* Relative proximity -> enforce curve connections (connect two strokes if they are close enough)


