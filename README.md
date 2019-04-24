<table>
  <thead>
    <tr>
      <th>Table of contents</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <details>
          <summary>Growth algorithms</summary>
          <p>
            <ul>
              <li><a href="#diffusion-limited-aggregation-dla">Diffusion-limited aggregation (DLA)</a></li>
              <li><a href="#differential-growth">Differential growth</a></li>
              <li><a href="#eden-growth-model">Eden growth model</a></li>
              <li><a href="#physarum">Physarum</a></li>
              <li><a href="#space-colonization">Space colonization</a></li>
              <li><a href="#reaction-diffusion">Reaction diffusion</a></li>
            </ul>
          </p>
        </details>
        <details>
          <summary>Mathematical topics</summary>
          <p>
            <ul>
              <li>Delaunay and voronoi diagrams</li>
              <li>Circle packing</li>
              <li>Cellular automata</li>
              <li>Fourier series</li>
              <li>Fractals</li>
              <li>Laplace transform</li>
              <li>Lissajous curves</li>
              <li>Navier-Stokes equations</li>
              <li>Strange Attractors</li>
              <li>Superellipse, supershapes, and superformula</li>
            </ul>
          </p>
        </details>
        <details>
          <summary>Lab experiments</summary>
          <p>
            <ul>
              <li>Hele-Shaw cell experiment</li>
              <li>Chladni plate</li>
              <li>Belousov–Zhabotinsky reaction</li>
            </ul>
          </p>
        </details>
        <details>
          <summary>Useful code patterns and techniques</summary>
          <p>
            <ul>
              <li>Particle systems</li>
              <li>Collision detection</li>
              <li>Spatial indexing</li>
              <li>Marching squares</li>
              <li>Marching cubes</li>
              <li>Noise (Perlin, Simplex)</li>
              <li>Physics libraries</li>
              <li>Signed distance functions (SDFs)</li>
            </ul>
          </p>
        </details>
        <details>
          <summary>Books</summary>
          <p>
            <ul>
            </ul>
          </p>
        </details>
      </td>
    </tr>
  </tbody>
</table>

## Growth algorithms

<img src="https://cdn-images-1.medium.com/max/600/1*0G4K7Z5_VQG8snj639vHbw.gif" width="300" height="300" align="right">

### Diffusion-limited aggregation (DLA)
Process in which particles of matter stick together (_aggregate_) as they chaotically move (_diffuse_) through a medium that provides some sort of resistive (_limiting_) force. As these particles clump together over time they form characteristic fractal branching structures known as [Brownian trees](https://medium.com/r/?url=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FBrownian_tree).

Very interesting macro-structures begin to emerge at around the 1-10 million particle range in 3D, but in order to get there you'll need to be smart about your rendering pipe and make use of optimized code in a performant language or environment (C/C++, CUDA, GLSL shaders, Houdini, etc).

_Key terms:_
* Walker - randomly-moving particle not attached to any other particle
* Cluster - group of multiple particles stuck together
* [Brownian tree](https://en.wikipedia.org/wiki/Brownian_tree) - name of characteristic branching structure that emerges

_Articles:_
* [Diffusion-limited aggregation](https://en.wikipedia.org/wiki/Diffusion-limited_aggregation) on Wikipedia
* [Diffusion-Limited Aggregation, a Kinetic Critical Phenomenon](http://ancient.hydro.nsc.ru/MPP_Specourse/witten81.pdf) (1981) by Thomas Witten and Leonard Sander. The article that started it all! _Note: visit your local library or a university library and ask a librarian if they can help you get free access!_
* [Diffusion-limited aggregation: A kinetic critical phenomenon?](http://www.thp.uni-koeln.de/krug/teaching-Dateien/SS2012/Sander2000.pdf) (2000) by Leonard Sander. Follow-up to the original article.
* [Simulating 2D diffusion-limited aggregation (DLA) with JavaScript](https://medium.com/@jason.webb/simulating-dla-in-js-f1914eb04b1d) by Jason Webb
* [DLA - Diffusion Limited Aggregation](http://paulbourke.net/fractals/dla/) by Paul Bourke
* [Diffusion-Limited Aggregation](https://softologyblog.wordpress.com/tag/diffusion-limited-aggregation/) by Softology
* [Pushing 3D Diffusion-Limited Aggregation even further](https://softologyblog.wordpress.com/2017/05/22/pushing-3d-diffusion-limited-aggregation-even-further/) by Softology

_Code projects:_
* [dlaf](https://github.com/fogleman/dlaf) (C++ w/ Boost) by Michael Fogleman <br><i>Introduces a novel, super-efficient method of collision detection, [described here](https://twitter.com/FogleBird/status/1093611865912025089).</i>
* [2D diffusion-limited aggregation (DLA) experiments in JavaScript](https://jasonwebb.github.io/2d-diffusion-limited-aggregation-experiments/) ([Github repo](https://github.com/jasonwebb/2d-diffusion-limited-aggregation-experiments)) by Jason Webb
* [Coding Challenge #34: Diffusion-Limited Aggregation](https://www.youtube.com/watch?v=Cl_Gjj80gPE) by Dan Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_034_DLA/P5))
* [Coding Challenge #127: Brownian Tree Snowflake](https://www.youtube.com/watch?v=XUA8UREROYE) by Dan Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_127_Snowflake_Brownian))
* [simutils-0001: Diffusion limited aggregation](http://toxiclibs.org/2010/02/new-package-simutils/) by Karsten Schmidt (toxiclibs)
* [Simulate: Diffusion-Limited Aggregation](http://formandcode.com/code-examples/simulate-dla) from FORM+CODE book examples
* [Dendron](http://www.flong.com/projects/dendron/) Processing sketch by Golan Levin
* 
_Notable software:_
* [Visions of Chaos](https://www.softology.com.au/voc.htm)

_Creative projects:_
* [Aggregation](http://www.andylomas.com/aggregation.html) series by Andy Lomas

<img src="https://cdn-images-1.medium.com/max/1000/1*3hSi1w_W-1YMW0YQaCk8rQ.gif" width="300" height="300" align="right">

### Differential growth
Process that acts on continuous chains of nodes connected by lines using simple rules (attraction, repulsion, alignment; not unlike boids) in order to produce undulating, buckling forms that mimic or simulate meandering rivers, rippled surface textures of plants/seeds/fruits, space-filling behaviors of worms, snakes, intestines, and much more.

_Articles and discussions:_
* [Exploring 2D differential growth with JavaScript](https://medium.com/@jason.webb/2d-differential-growth-in-js-1843fd51b0ce) by Jason Webb
* [Differential line](https://inconvergent.net/generative/differential-line/) by Anders Hoff (inconvergent)
* [Sheparding Random Growth](https://inconvergent.net/2016/shepherding-random-growth/) by Anders Hoff (inconvergent)
* [Differential Mesh Growth discussion thread](https://forums.odforce.net/topic/25534-differential-curve-growth/) on od|force forums
* [Organic Labrynths and Mazes](http://www.dgp.toronto.edu/~karan/artexhibit/mazes.pdf) (PDF) paper by Hans Pederson and Karen Singh

_Code projects:_
* [2D differential growth experiments](https://jasonwebb.github.io/2d-differential-growth-experiments/) by Jason Webb ([Github repo](https://github.com/jasonwebb/2d-differential-growth-experiments))
* [Differential line growth with Processing](http://www.codeplastic.com/2017/07/22/differential-line-growth-with-processing/) by Alberto Giachino
* [Real-time differential growth in JavaScript](http://adrianton3.github.io/blog/art/differential-growth/differential-growth.html) by [Adrian Toncean](https://github.com/adrianton3)
* [Differential Line Growth](http://www.entagma.com/differential-line-growth/) by Maritz Schwind of Entagma
* [Differential Growth](https://codepen.io/MAKIO135/pen/EwYPmb) by Lionel Radisson

_Creative projects:_
* [Floraform - an exploration of differential growth](https://n-e-r-v-o-u-s.com/blog/?p=6721) by Nervous System
* [Floraform Chandelier at World Expo 2017 in Astana, Kazakhstan](https://n-e-r-v-o-u-s.com/blog/?p=7702) by Nervous System

<img src="https://cdn.iopscience.com/images/1742-5468/2006/11/P11007/Full/3564901.jpg" width="150" align="right">

### Eden growth model
Created by Murray Eden in 1961, this is a type of surface fractal growth process where material randomly accumulates on the _boundary_ of clusters. Sort of like DLA but without all the empty space between branches. Thought to be a good way to model certain kinds of bacterial and lichen growth.

_Articles:_
* [A Two Dimensional Growth Process](https://projecteuclid.org/download/pdf_1/euclid.bsmsp/1200512888) by Murray Eden (original 1961 paper)

### Physarum
_Articles:_
* [Physarum Simulations](https://softologyblog.wordpress.com/2019/04/11/physarum-simulations/) by Softology

### Space colonization
### Reaction-diffusion

## Mathematical topics
<img src="https://c1.staticflickr.com/1/915/42277964325_431501c7c0_o.gif" width="300" align="right">

### Cellular automata (CA)
A regular grid of _cells_ with _states_ that are updated each iteration in accordance with _rules_. Developed by Stanislaw Ulam and John von Neumann at the Los Alamos National Laboratory in the 1940s, this system can be used to model physical, biological, and social phenomena

_Key terms:_
* Cell - a discrete location on the grid
* State - the "value" of a cell. Many CAs just have two states (on/off), but others use many.
* Neighborhood - set of cells surrounding a given cell. Most common types are [Von Neumann](https://en.wikipedia.org/wiki/Von_Neumann_neighborhood) and [Moore](https://en.wikipedia.org/wiki/Moore_neighborhood), though others exist.
* Rule(s) - if/else statement(s) that define what the next state of a cell should be based on various criteria like the states of that cell's neighbors.
* Generation - result of one iteration of the system.

_Well-known rules:_
* Game of Life
* Langton's Ant
* Brian's Brain

_Articles:_
* [Cellular automaton](https://en.wikipedia.org/wiki/Cellular_automaton) on Wikipedia
* [Elementary Cellular Automaton](http://mathworld.wolfram.com/ElementaryCellularAutomaton.html) on Wolfram MathWorld
* [Chapter 7. Cellular Automata](https://natureofcode.com/book/chapter-7-cellular-automata/) from Daniel Shiffman's Nature of Code book

_Notable software:_
* [MCell](http://psoup.math.wisc.edu/mcell/) (Mirek's Cellebration)
* [Golly](http://golly.sourceforge.net/)
* [Visions of Chaos](https://www.softology.com.au/voc.htm)

<img src="https://i.imgur.com/iOr8mvo.png" width="300" align="right">

### Delaunay triangulation and Voronoi diagrams
_Delaunay triangulation_ is a way to connect a set of points

_Articles:_
* [Delaunay triangulation](https://en.wikipedia.org/wiki/Delaunay_triangulation) on Wikipedia
* [Voronoi diagram](https://en.wikipedia.org/wiki/Voronoi_diagram) on Wikipedia

### Fourier series

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Mandel_zoom_08_satellite_antenna.jpg/320px-Mandel_zoom_08_satellite_antenna.jpg" width="300" align="right">

### Fractals
Infinitely complex patterns that are self-similar across all scales

_Notable fractals:_
* [Apollonian gasket](https://en.wikipedia.org/wiki/Apollonian_gasket) (a.k.a. curvilinear Sierpiński gasket)
* [Barnsley fern](https://en.wikipedia.org/wiki/Barnsley_fern)
* [Cantor set](https://en.wikipedia.org/wiki/Cantor_set)
* [Chaos game](https://en.wikipedia.org/wiki/Chaos_game)
* [Dragon curve](https://en.wikipedia.org/wiki/Dragon_curve)
* [Hilbert curve](https://en.wikipedia.org/wiki/Hilbert_curve)
* [Iterated function systems (IFS)](https://en.wikipedia.org/wiki/Iterated_function_system)
  * [Lindenmayer systems (L-systems)](https://en.wikipedia.org/wiki/L-system)
* [Julia set](https://en.wikipedia.org/wiki/Julia_set)
* [Koch snowflake](https://en.wikipedia.org/wiki/Koch_snowflake)
* [Menger sponge](https://en.wikipedia.org/wiki/Menger_sponge)
* [Mandelbrot set](https://en.wikipedia.org/wiki/Mandelbrot_set) (related: [Mandelbulb](https://en.wikipedia.org/wiki/Mandelbulb) and [Buddhabrot](https://en.wikipedia.org/wiki/Buddhabrot))
* [Sierpiński triangle / gasket / sieve](https://en.wikipedia.org/wiki/Sierpi%C5%84ski_triangle) and [carpet](https://en.wikipedia.org/wiki/Sierpinski_carpet)
* [... and so much more](https://en.wikipedia.org/wiki/List_of_fractals_by_Hausdorff_dimension)

_Articles:_
* [Fractal](https://en.wikipedia.org/wiki/Fractal) on Wikipedia
* [List of fractals by Hausdorff dimension](https://en.wikipedia.org/wiki/List_of_fractals_by_Hausdorff_dimension) on Wikipedia

### Laplace transform
### Lissajous curves
### Navier-Stokes equations
### Packing problems
* Circle packing
* See [Packing problems](https://en.wikipedia.org/wiki/Packing_problems) on Wikipedia

### Strange Attractors
* Clifford attractors
* Lorenz attractors
* Duffing attractor
* Rossler attractor
* Bouali attractor
* Henon attractor

### Superellipse, supershapes, and superformula
### Travelling salesman problem (TSP)
Asks the question "Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city and returns to the origin city?" This classic problem is computer science classrooms to teach algorithm design and optimization techniques.

_Useful for:_
* Creating single-line drawings for use with pen plotters, laser cutters, CNC machines, and more.

_Articles:_
* [Travelling salesman problem](https://en.wikipedia.org/wiki/Travelling_salesman_problem) on Wikipedia

_Notable software:_
* [StippleGen](https://wiki.evilmadscientist.com/StippleGen) from Evil Mad Scientist Laboratories can [calculate TSP paths](https://wiki.evilmadscientist.com/StippleGen#Calculating_the_TSP_Path).

## Lab experiments
* Hele-Shaw cell experiment
* Chladni plate
* Belousov–Zhabotinsky reaction

## Useful code patterns and techniques
* Collision detection
* Marching squares
* Marching cubes
* Noise (Perlin, Simplex)
* Particle systems
* Physics libraries
* Signed distance functions (SDFs)
* Spatial indexing
* Metaballs

## Books
* [On Growth and Form](https://smile.amazon.com/Growth-Form-Complete-Revised/dp/0486671356/) by D'Arcy Wentworth Thompson
* Nature's Patterns: A Tapestry in Three Parts by Philip Ball
  * [Flow](https://smile.amazon.com/Flow-Natures-Patterns-Tapestry-Three/dp/0199604878/)
  * [Branches](https://smile.amazon.com/Branches-Natures-Patterns-Tapestry-Three/dp/0199604886/)
  * [Shapes](https://smile.amazon.com/Shapes-Natures-Patterns-Tapestry-Three/dp/0199237964/)
* [Fractal Concepts in Surface Growth](https://smile.amazon.com/Fractal-Concepts-Surface-Albert-Laszlo-Barabasi/dp/0521483182) by Albert-László Barabási
* [Fractal Growth Phenomena](https://smile.amazon.com/gp/product/9810206690/) by Tamas Vicsek  

## Uncategorized (TODO)
* Phyllotaxis
* Inverse and forward kinematics
* Cymatics
* Turing patterns
* Viscous fingering, a.k.a. Saffman–Taylor instability