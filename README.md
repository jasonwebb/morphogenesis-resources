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
              <li><a href="#dielectric-breakdown-model-dbm">Dielectric breakdown model (DBM)</a></li>
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
              <li><a href="#cellular-automata-ca">Cellular automata</a></li>
              <li><a href="#delaunay-triangulation-and-voronoi-diagrams">Delaunay triangulation and Voronoi diagrams</a></li>
              <li><a href="#fourier-series">Fourier series</a></li>
              <li><a href="#fractals">Fractals</a></li>
              <li><a href="#laplace-transform">Laplace transform</a></li>
              <li><a href="#lissajous-curves">Lissajous curves</a></li>
              <li><a href="#navier-stokes-equations">Navier-Stokes equations</a></li>
              <li><a href="#packing-problems">Packing problems</a></li>
              <li><a href="#strange-attractors">Strange attractors</a></li>
              <li><a href="#superellipse">Superellipse</a></li>
              <li><a href="#superformula">Superformula</a></li>
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
        ▸ <a href="#books">Books</a><br>
        ▸ <a href="#software">Software</a>
      </td>
    </tr>
  </tbody>
</table>

## Growth algorithms

### Dielectric breakdown model (DBM)

```
TODO
```

_Articles:_
* [Fractal Dimension of Dielectric Breakdown](http://laplace.ucv.cl/Patterns/Referencias/Pietronero-prl52-1033.pdf) (PDF) by L. Niemeyer, L. Pietronero, and H. J. Wiesmann

---

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
* [simutils-0001: Diffusion limited aggregation](http://toxiclibs.org/2010/02/new-package-simutils/) by Karsten Schmidt (toxiclibs)
* [Simulate: Diffusion-Limited Aggregation](http://formandcode.com/code-examples/simulate-dla) from FORM+CODE book examples
* [Dendron](http://www.flong.com/projects/dendron/) Processing sketch by Golan Levin

_Creative projects:_
* [Aggregation](http://www.andylomas.com/aggregation.html) series by Andy Lomas

_Notable software:_
* [Visions of Chaos](https://www.softology.com.au/voc.htm)
* [glChAoS.P](https://github.com/BrutPitt/glChAoS.P) by Michele Morrone (BrutPitt)

_Videos:_
* [Coding Challenge #34: Diffusion-Limited Aggregation](https://www.youtube.com/watch?v=Cl_Gjj80gPE) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_034_DLA/P5))
* [Coding Challenge #127: Brownian Tree Snowflake](https://www.youtube.com/watch?v=XUA8UREROYE) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_127_Snowflake_Brownian))


---

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

---

<img src="https://cdn.iopscience.com/images/1742-5468/2006/11/P11007/Full/3564901.jpg" width="150" align="right">

### Eden growth model
Created by Murray Eden in 1961, this is a type of surface fractal growth process where material randomly accumulates on the _boundary_ of clusters. Sort of like DLA but without all the empty space between branches. Thought to be a good way to model certain kinds of bacterial and lichen growth.

_Articles:_
* [A Two Dimensional Growth Process](https://projecteuclid.org/download/pdf_1/euclid.bsmsp/1200512888) by Murray Eden (original 1961 paper)

---

### Physarum

```
TODO
```

_Articles:_
* [Physarum Simulations](https://softologyblog.wordpress.com/2019/04/11/physarum-simulations/) by Softology
* [Physarum polycephalum](https://en.wikipedia.org/wiki/Physarum_polycephalum) on Wikipedia

---

### Space colonization

```
TODO
```

_Articles:_
* [Modeling Trees with a Space Colonization Algorithm](http://algorithmicbotany.org/papers/colonization.egwnp2007.large.pdf) (PDF) paper by Adam Runions, Brendan Lane, and Przemyslaw Prusinkiewicz

_Code projects:_
* [ofxSpaceColoinzation](https://github.com/edap/ofxSpaceColonization) add-on for openFrameworks

_Videos:_
* [Coding Challenge #17: Fractal Trees - Space Colonization](https://www.youtube.com/watch?v=kKT0v3qhIQY) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_017_SpaceColonizer) with source code for p5.js and Processing)

---

### Reaction-diffusion

```
TODO
```

_Key terms:_
* Gray Scott model

_Articles:_
* [Reaction-diffusion system](https://en.wikipedia.org/wiki/Reaction%E2%80%93diffusion_system) on Wikipedia
* [Reaction-Diffusion Tutorial](https://www.karlsims.com/rd.html) by Karl Sims
* [Reaction-Diffusion by the Gray-Scott Model: Pearson's Parametrization](https://mrob.com/pub/comp/xmorphia/) by Robert Munafo (mrob)
* [Reaction Diffusion: The Gray-Scott Algorithm](https://www.algosome.com/articles/reaction-diffusion-gray-scott.html) by Algosome

_Videos:_
* Reaction Diffusion video series for Houdini by Entagma:
  * [Part I: Theory](https://vimeo.com/170073061)
  * [Part II: Implementation](https://vimeo.com/170073069)
  * [Part III: Shaping Growth](https://vimeo.com/170073079)
* [Coding Challenge #13: Reaction Diffusion Algorithm in p5.js](https://www.youtube.com/watch?v=BV9ny785UNc) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_013_ReactionDiffusion) with both p5.js and Processing source code)

## Mathematical topics
<img src="https://c1.staticflickr.com/1/915/42277964325_431501c7c0_o.gif" width="300" align="right">

### Cellular automata (CA)
A regular grid of _cells_ with _states_ that are updated each iteration in according to _rules_. Developed by Stanislaw Ulam and John von Neumann at the Los Alamos National Laboratory in the 1940s, this system has been used to model physical, biological, and social phenomena with remarkable variety and accuracy. 

_Key terms:_
* Cell - a discrete location on the grid
* State - the "value" of a cell. Many CAs just have two states (on/off), but others use many.
* Neighborhood - set of cells surrounding a given cell. Most common types are [Von Neumann](https://en.wikipedia.org/wiki/Von_Neumann_neighborhood) and [Moore](https://en.wikipedia.org/wiki/Moore_neighborhood), though others exist.
* Rule(s) - if/else statement(s) that define what the next state of a cell should be based on various criteria like the states of that cell's neighbors.
* Generation - result of one iteration of the system.

_Well-known rules:_
* [Brian's Brain](https://en.wikipedia.org/wiki/Brian%27s_Brain)
* [Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life)
* [Langton's Ant](https://en.wikipedia.org/wiki/Langton%27s_ant)
* [Wireworld](http://mathworld.wolfram.com/WireWorld.html)

_Articles:_
* [Cellular automaton](https://en.wikipedia.org/wiki/Cellular_automaton) on Wikipedia
* [Elementary Cellular Automaton](http://mathworld.wolfram.com/ElementaryCellularAutomaton.html) on Wolfram MathWorld
* [Chapter 7. Cellular Automata](https://natureofcode.com/book/chapter-7-cellular-automata/) from Daniel Shiffman's Nature of Code book

_Notable software:_
* [MCell](http://psoup.math.wisc.edu/mcell/) (Mirek's Cellebration)
* [Golly](http://golly.sourceforge.net/)
* [Visions of Chaos](https://www.softology.com.au/voc.htm)

---

<img src="https://i.imgur.com/iOr8mvo.png" width="300" align="right">

### Delaunay triangulation and Voronoi diagrams
_Delaunay triangulation_ is a way of connecting a set of points to form a network of non-overlapping triangles. One of the key properties of Delaunay triangulations is that the [circumcircles](https://en.wikipedia.org/wiki/Circumscribed_circle) associated with each triangle contains no other points than their three triangle vertices. When extended into 3D, Delaunay triangulation is useful for creating meshes.

_Voronoi diagrams_ are the [dual](https://observablehq.com/@mbostock/the-delaunays-dual) of Delaunay triangulations. This means that once a Delaunay triangulation has been computed for a set of points, a Voronoi diagram can be drawn without any additional data - just draw lines connecting the centers of the circumcircles! 

_Voronoi diagrams_ are very useful for efficiently and organically partitioning (splitting up) both 2D and 3D space. They are especially good for accurately modelling the way soft bodies (like biological cells) get smushed together in constrained environments, like embryonic cells undergoing mitosis.

_Articles:_
* [Delaunay triangulation](https://en.wikipedia.org/wiki/Delaunay_triangulation) on Wikipedia
* [Voronoi diagram](https://en.wikipedia.org/wiki/Voronoi_diagram) on Wikipedia

---

### Fourier series

```
TODO
```

* [Coding Challenge #125: Fourier Series](https://www.youtube.com/watch?v=Mm2eYfj0SgA) by Daniel Shiffman
* [Coding Challenge #130.1: Drawing with Fourier Transform and Epicycles](https://www.youtube.com/watch?v=MY4luNgGfms) by Daniel Shiffman
* [Coding Challenge #130.2: Fourier Transform User Drawing](https://www.youtube.com/watch?v=n9nfTxp_APM) by Daniel Shiffman
* [Coding Challenge #130.3: Fourier Transform Drawing with Complex Number Input](https://www.youtube.com/watch?v=7_vKzcgpfvU) by Daniel Shiffman

---

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Mandel_zoom_08_satellite_antenna.jpg/320px-Mandel_zoom_08_satellite_antenna.jpg" width="300" align="right">

### Fractals
Infinitely complex patterns generated via recursion that are self-similar across all scales. Thought to be found in abundance in nature, though "true" (infinite) fractals are not possible because nature uses physical matter, which has particular structures at the microscopic and smaller scales (molecules, atoms, elementary particles, etc).

Fractal features can be observed in nature in tree branching structures, leaf veins, terrain, surface textures, coastlines, rivers, succulents, snowflakes, rivers, lightning bolts, nautilus shells (both form and pattern), and so much more.

_Key terms:_
* [Fractal dimension](https://en.wikipedia.org/wiki/Fractal_dimension) - ratio providing a statistical index of complexity comparing how detail in a fractal changes with scale.
* [Self-similarity](https://en.wikipedia.org/wiki/Self-similarity) - when something is exactly or approximately similar to a part of itself.

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
* [Fractals, Caos, Self-Similarity](http://paulbourke.net/fractals/) by Paul Bourke
* [Chapter 8. Fractals](https://natureofcode.com/book/chapter-8-fractals/) in Daniel Shiffman's Nature of Code book

_Notable software:_
* [glChAoS.P](https://github.com/BrutPitt/glChAoS.P) by Michele Morrone (BrutPitt)

---

### Laplace transform

```
TODO
```

<img src="https://media3.giphy.com/media/I6eLbjpGq99x6/giphy.gif" width="300" align="right">

---

### Lissajous curves

```
TODO
```

_Articles:_
* [Lissajous curve](https://en.wikipedia.org/wiki/Lissajous_curve) on Wikipedia

---

### Medial axis

```
TODO
```

---

### Navier-Stokes equations
Mathematical equation that describe the motion of viscous fluids.

_Articles:_
* [Navier-Stokes equations](https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations) on Wikipedia

---

### Packing problems

```
TODO
```

* Circle packing

_Articles:_
* [Packing problems](https://en.wikipedia.org/wiki/Packing_problems) on Wikipedia
* [Random space filling of the plane](http://paulbourke.net/fractals/randomtile/) by Paul Bourke

---

### Spherical harmonics

```
TODO
```

_Articles:_
* [Spherical harmonics](https://en.wikipedia.org/wiki/Spherical_harmonics) on Wikipedia
* [Spherical Harmonics](http://paulbourke.net/geometry/sphericalh/) by Paul Bourke

---

<img src="https://upload.wikimedia.org/wikipedia/commons/4/4a/Attractor_Poisson_Saturne.jpg" width="200" align="right">

### Strange attractors

```
TODO
```

_Notable attractors:_
* [Clifford attractor](http://paulbourke.net/fractals/clifford/)
* [Duffing attractor](http://paulbourke.net/fractals/duffing/)
* [Hénon attractor](https://en.wikipedia.org/wiki/H%C3%A9non_map)
* [Lorenz attractor](https://en.wikipedia.org/wiki/Lorenz_system)
* [Multiscroll attractor](https://en.wikipedia.org/wiki/Multiscroll_attractor) (a.k.a double-scroll attractor or Chua's attractor)
* [Rössler attractor](https://en.wikipedia.org/wiki/R%C3%B6ssler_attractor)

_Articles:_
* [Strange attractor](https://en.wikipedia.org/wiki/Attractor#Strange_attractor) section on Wikipedia article for [attractors](https://en.wikipedia.org/wiki/Attractor)

---

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/Sf2d.png/800px-Sf2d.png" width="300" align="right">

### Superellipse

Also known as the Lamé curve, this equation describes a closed curve that can generate shapes that look like pinched or inflated ellipses. At the extremes of the parameter space the shapes can range from an outline of a plus (`+`) symbol to a nearly rectangular shape with rounded corners. 

_Equations:_
<table>
 <tr>
  <td valign="top">General form</td>
  <td><img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/2b21da32fe407ff5714620b26c50343d21afed15"></td>
 </tr>
 <tr>
  <td valign="top">Parametric</td>
  <td><img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/5ecc6bff4267f2ec1ee1d16845b8c402009880ea"></td>
 </tr>
</table>

_Articles:_
* [Superellipse](https://en.wikipedia.org/wiki/Superellipse) on Wikipedia

_Videos:_
* [Coding Challenge #23: 2D Supershapes](https://www.youtube.com/watch?v=ksRoh-10lak) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_023_SuperShape2D) with Processing and p5.js code)

---

<a href="https://github.com/Softwave/glsl-superformula" target="_blank"><img src="https://camo.githubusercontent.com/5da22383c27146107d848fd73659ba12e2a38d4a/687474703a2f2f692e696d6775722e636f6d2f744131755263662e706e67" width="300" align="right" alt="Screenshot from GLSL Supershapes by Softwave"></a>

### Superformula
Generalized version of the superellipse formula proposed by Johan Giellis around 2000, capable of far more variety than the original superellipse. Unfortunately, Johan has patented use of the formula (via his company [Genicap](http://www.genicap.com/)) in both the US and the EU, which means you should avoid using it for any kind of commercial work, or work that could be commercialized in some way later. 

The superformula can be used to generate both 2D and 3D forms. To create 2D forms, use the general form equation to obtain [polar coordinates](http://mathworld.wolfram.com/PolarCoordinates.html) that can be converted into Cartesian coordinates for drawing on a screen. To create 3D forms, compute the polar coordinates for _two_ 2D supershapes, then "mix" them together using the 3D equations below.

_Equations:_
<table>
 <tr>
  <td valign="top">General form</td>
  <td>
   <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/8071dcb3a49044816f7885114c2335d805d7ad30"> 

   Where `r` is a radius and `φ` (phi) is an angle
  </td>
 </tr>
 <tr>
  <td valign="top">3D equations</td>
  <td>
   <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/4859fbe75c6a60f5769bebb1376693343c1aa3bd"><br>
   <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/f5b68c1caf5b0bf4b912a6f8c7278f004774952a"><br>
   <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/a8396e4a1a6c4dd9a7466e714c8a2759e4e95f82">

   Where `φ` (latitude) varies between −π/2 and π/2 and `θ` (longitude) between −π and π.
  </td>
 </tr>
</table>

_Parameters:_

| Param | Effect (loosely) |
|---    |---               |
| `a`   | |
| `b`   | |
| `m1`  | |
| `m2`  | |
| `n1`  | |
| `n2`  | |
| `n3`  | |

_Articles:_
* [Superformula](https://en.wikipedia.org/wiki/Superformula) on Wikipedia
* [Supershapes / Superformula](http://paulbourke.net/geometry/supershape/) by Paul Bourke

_Videos:_
* [Coding Challenge #26: 3D Supershapes](https://www.youtube.com/watch?v=akM4wMZIBWg) by Daniel Shiffman ([Processing sketch](https://github.com/CodingTrain/website/blob/master/CodingChallenges/CC_026_SuperShape3D/Processing/CC_026_SuperShape3D/CC_026_SuperShape3D.pde) on Github)

---

<img src="http://mathworld.wolfram.com/images/eps-gif/TravelingSalesmanProblem_1000.gif" width="300" align="right">

### Travelling salesman problem (TSP)
Asks the question "Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city and returns to the origin city?" This classic problem is computer science classrooms to teach algorithm design and optimization techniques.

Useful for creating single-line drawings for use with pen plotters, laser cutters, CNC machines, and more.

_Articles:_
* [Travelling salesman problem](https://en.wikipedia.org/wiki/Travelling_salesman_problem) on Wikipedia
* [Traveling Salesman Problem](https://developers.google.com/optimization/routing/tsp) from Google OR-Tools

_Notable software:_
* [StippleGen](https://wiki.evilmadscientist.com/StippleGen) from Evil Mad Scientist Laboratories can [calculate TSP paths](https://wiki.evilmadscientist.com/StippleGen#Calculating_the_TSP_Path).

## Lab experiments

### Hele-Shaw cell experiment

```
TODO
```

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a1/Quadratic_Chladni_plate.JPG/760px-Quadratic_Chladni_plate.JPG" width="300" align="right">

### Chladni plate

```
TODO
```

### Belousov–Zhabotinsky reaction

```
TODO
```

## Useful code patterns and techniques
* Collision detection
* Dithering
* Marching squares
* Marching cubes
* Noise (Perlin, Simplex)
* Particle systems
* Physics libraries
* Recursion (fractals, especially IFS)
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

## Software

### Tools
<table>
  <thead>
    <tr>
      <td>Application</td>
      <td>Description</td>
      <td>Cost</td>
      <td>Plugins</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top">[Houdini](https://www.sidefx.com/products/houdini/)</td>
      <td>Industry-level procedural VFX application with graphical node-based workflow. Excellent for creating high-quality renderings and animations based on generative algorithms.</td>
      <td>Free for non-commercial users (with watermarked renders)
      $269 for no watermarks, thousands for studios)</td>
      <td></td>
    </tr>
    <tr>
      <td>[Rhino](https://www.rhino3d.com/)</td>
      <td>NURBS-based CAD program popular with architects and designers.</td>
      <td>$1000, or $200 for students</td>
      <td>
        <ul>
          <li>[Grasshopper](https://www.grasshopper3d.com/) - extremely popular graphical node-based algorithm editor tightly integrated with Rhino’s 3D modeling tools. Highly recommended for digital morphogenesis work. Was a third-party plugin for many years, but is now a part of Rhino 6+.</li>
          <li>[Lunchbox](https://www.food4rhino.com/app/lunchbox) - very powerful collection of utilities for generative geometry, math, data manipulation, and even machine learning.</li>
          <li>[Kangaroo](https://www.food4rhino.com/app/kangaroo-physics) - live physics engine for interactive simulation, form-finding, optimization and constraint solving.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

* [Structure Synth](http://structuresynth.sourceforge.net/) (free) - application for generating surprising and complex fractal 3D structures using a design grammar.
* [TouchDesigner](https://www.derivative.ca/) ($)
* [Unity](https://unity.com/) (free for hobbyists [[1]](https://store.unity.com/))
  * [Visual Effects Graph](https://unity.com/visual-effect-graph) (VFX Graph)
* [Unreal](https://www.unrealengine.com/en-US/) (free with [royalty on commercial products](https://www.unrealengine.com/en-US/faq))

### Languages and frameworks
* Shaders (GLSL / GLslang / OpenGL Shader Language)
  * [Shadertoy](https://www.shadertoy.com/)
* C++
  * [boost](https://www.boost.org/)
  * [Cinder](https://www.libcinder.org/)
  * [openFrameworks](https://openframeworks.cc/)
* Go
* JavaScript
  * [p5.js](https://p5js.org/)
  * [D3.js](https://d3js.org/)
  * [three.js](https://threejs.org/)
  * [Pts.js](https://ptsjs.org/)
  * [sketch.js](http://soulwire.github.io/sketch.js/)
* Java
  * [Processing](https://processing.org/)
* Rust
  * [nannou](https://github.com/nannou-org/nannou)
* Kotlin
  * [OPENRNDR](https://openrndr.org/)

## Uncategorized (TODO)
* Phyllotaxis
* Inverse and forward kinematics
* Cymatics
* Turing patterns
* Viscous fingering, a.k.a. Saffman–Taylor instability