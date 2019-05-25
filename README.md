[Digital morphogenesis](https://en.wikipedia.org/wiki/Digital_morphogenesis) is the exploration of how shapes, forms, and patterns emerge in nature through the use of computational modeling and generative systems based on biological, chemical, and physical processes. It draws upon research from practically every area of the natural sciences and has applications in architecture, digital fabrication, art, engineering, biomedicine, and more. 

With such a cross-disciplinary topic it can be hard to keep track of and correlate all the interesting bits of knowledge that one comes across, which is where this list comes in. The goal of this list is to succinctly catalog various growth algorithms and lab experiments along with relevant math, physics, and programming concepts in one place in order to (1) serve as a sort of "cheat sheet" reference for developers and computer artists, and (2) spark new insights by making it easier to see relationships between seemingly disparate topics.

<br>

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
              <li><a href="#primordial-particle-system">Primordial Particle System</a></li>
              <li><a href="#space-colonization">Space colonization</a></li>
              <li><a href="#reaction-diffusion">Reaction diffusion</a></li>
            </ul>
          </p>
        </details>
        <details>
          <summary>Math and physics topics</summary>
          <p>
            <ul>
              <li><a href="#cellular-automata-ca">Cellular automata</a></li>
              <li><a href="#cymatics">Cymatics</a></li>
              <li><a href="#delaunay-triangulation-and-voronoi-diagrams">Delaunay triangulation and Voronoi diagrams</a></li>
              <li><a href="#fibonacci-sequence">Fibonacci sequence</a></li>
              <li><a href="#fluid-simulation">Fluid simulation</a></li>
              <li><a href="#fourier-series">Fourier series</a></li>
              <li><a href="#fractals">Fractals</a></li>
              <li><a href="#golden-angle">Golden angle</a></li>
              <li><a href="#golden-ratio">Golden ratio</a></li>
              <li><a href="#inverse-and-forward-kinematics">Inverse and forward kinematics</a></li>
              <li><a href="#laplace-transform">Laplace transform</a></li>
              <li><a href="#lissajous-curves">Lissajous curves</a></li>
              <li><a href="#minimal-surface">Minimal surface</a></li>
              <li><a href="#packing-problems">Packing problems</a></li>
              <li><a href="#phyllotaxis">Phyllotaxis</a></li>
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
              <li><a href="#belousovzhabotinsky-reaction">Belousov–Zhabotinsky reaction</a></li>
              <li><a href="#chladni-plate">Chladni plate</a></li>
              <li><a href="#hele-shaw-cell-experiment">Hele-Shaw cell experiment</a></li>
              <li><a href="#schlieren-imaging">Schlieren imaging</a></li>
            </ul>
          </p>
        </details>
        <details>
          <summary>Useful code patterns and techniques</summary>
          <p>
            <ul>
              <li><a href="#agentbased-modelling">Agent-based modelling</a></li>
              <li><a href="#collision-detection">Collision detection</a></li>
              <li><a href="#dithering">Dithering</a></li>
              <li><a href="#marching-squares">Marching squares</a></li>
              <li><a href="#marching-cubes">Marching cubes</a></li>
              <li><a href="#metaballs">Metaballs</a></li>
              <li><a href="#noise">Noise</a></li>
              <li><a href="#particle-system">Particle system</a></li>
              <li><a href="#physics-engine">Physics engine</a></li>
              <li><a href="#recursion">Recursion</a></li>
              <li><a href="#shaders">Shaders</a></li>
              <li><a href="#signed-distance-function-sdfs">Signed distance functions (SDFs)</a></li>
              <li><a href="#spatial-index">Spatial index</a></li>
              <li><a href="#wave-function-collapse-wfc">Wave Function Collapse (WFC)</a></li>
            </ul>
          </p>
        </details>
        ▸ <a href="#books-and-publications">Books and publications</a><br>
        ▸ <a href="#software">Software</a>
      </td>
    </tr>
  </tbody>
</table>

<br>

## Growth algorithms

### Dielectric breakdown model (DBM)

```
TODO
```

* Rigid and elastic bond models

_Articles:_
* [Dielectric breakdown model](https://en.wikipedia.org/wiki/Dielectric_breakdown_model) on Wikipedia
* [Fractal Dimension of Dielectric Breakdown](http://laplace.ucv.cl/Patterns/Referencias/Pietronero-prl52-1033.pdf) (PDF) by L. Niemeyer, L. Pietronero, and H. J. Wiesmann

---

<img src="https://cdn-images-1.medium.com/max/600/1*0G4K7Z5_VQG8snj639vHbw.gif" width="300" height="300" align="right">

### Diffusion-limited aggregation (DLA)
Process in which particles of matter stick together (_aggregate_) as they chaotically move (_diffuse_) through a medium that provides some sort of resistive (_limiting_) force. As these particles clump together over time they form characteristic fractal branching structures known as [Brownian trees](https://medium.com/r/?url=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FBrownian_tree).

Very interesting macro-structures begin to emerge at around the 1-10 million particle range in 3D, but in order to get there you'll need to be smart about your rendering pipeline and make use of optimized code in a performant language or environment (C/C++, CUDA, GLSL shaders, Houdini, etc).

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
* [VEX in Houdini: Diffusion Limited Aggregation (Plus Rendering In Mantra & Redshift)](https://vimeo.com/218372128) by Entagma


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
* [Characteristics of Pattern Formation and Evolution in Approximations of Physarum Transport Networks](http://eprints.uwe.ac.uk/15260/1/artl.2010.16.2.pdf) (PDF) by Jeff Jones - original paper
* [Physarum Simulations](https://softologyblog.wordpress.com/2019/04/11/physarum-simulations/) by Softology
* [Physarum polycephalum](https://en.wikipedia.org/wiki/Physarum_polycephalum) on Wikipedia

_Code projects:_
* [Simulating slime mold with WebGL](https://kaesve.nl/projects/mold/summary.html) by Ken Voskuil

_Creative projects:_
* [physarum](https://sagejenson.com/physarum) by Sage Jenson (mxsage)
* [Slime mold](http://ch3.gr/2018/slime-mold/) by Georgios Cherouvim

---

### Primordial Particle System

```
TODO
```

_Articles:_
* [Primordial Particle Systems](http://zool33.uni-graz.at/artlife/PPS) from the Artificial Life Laboratory in Graz, Austria.
* [How a life-like system emerges from a simple particle motion law](https://www.nature.com/articles/srep37969) Thomas Schmickl, Martin Stefanec & Karl Crailsheim

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

<img src="https://cdna.artstation.com/p/assets/images/images/008/781/346/large/pascal-wiemers-new-graph-basecolor-17.jpg?1515275614" width="250" align="right">

### Reaction-diffusion

Grid-based process that generates complex and dynamic patterns based the interactions of two chemicals as they _diffuse_ through a medium. At every location on the grid these chemicals (usually referred to as `A` and `B`) have a chance of causing a _reaction_ that converts chemicals of one type to another based on their relative concentrations at that location. 

Throughout the simulation chemical `A` is added at a particular _feed rate_ (`f`) and chemical `B` is removed at a particular _kill rate_ (`k`) - adjusting these rates can result in wildly different emergent patterns.

_Equation (via [Karl Sims](https://www.karlsims.com/rd.html)):_
![Reaction-diffusion equation from Karl Sims](https://www.karlsims.com/rd-equation.png)

_Key terms:_
* Feed rate - rate at which chemical `A` is added to system
* Kill rate - rate at which chemical `B` is removed from the system
* Diffusion rate - rate at which each chemical spreads, which acts as a kind of scaler to a 3x3 [Laplacian transform](#laplace-transform)
* Reaction chance - probability that one `A` will be converted to a `B` when in the presence of two `B`s.
* Gray-Scott model
* [Pearson's classification](http://mrob.com/pub/comp/xmorphia/pearson-classes.html)
* [Turing patterns](https://en.wikipedia.org/wiki/Turing_pattern)

_Articles:_
* [Reaction-diffusion system](https://en.wikipedia.org/wiki/Reaction%E2%80%93diffusion_system) on Wikipedia
* [Reaction-Diffusion Tutorial](https://www.karlsims.com/rd.html) by Karl Sims
* [Reaction-Diffusion by the Gray-Scott Model: Pearson's Parametrization](https://mrob.com/pub/comp/xmorphia/) by Robert Munafo (mrob)
* [Reaction Diffusion: The Gray-Scott Algorithm](https://www.algosome.com/articles/reaction-diffusion-gray-scott.html) by Algosome
* [The Chemical Basis of Morphogenesis](http://www.dna.caltech.edu/courses/cs191/paperscs191/turing.pdf) (PDF) paper by Alan Turing (1951)

_Code projects:_
* [simutils-0001: Gray-Scott reaction diffusion](http://toxiclibs.org/2010/02/simutils-grayscott/) by toxiclibs
* [ofxReactionDiffusion](https://github.com/matsune/ofxReactionDiffusion) add-on for openFrameworks by Yuma Matsune
* [ofxRD](https://github.com/aanrii/ofxRD) add-on for openFrameworks by aanrii

_Creative projects:_
* [3D Printed Reaction Diffusion Patterns](https://www.instructables.com/id/3D-Printed-Reaction-Diffusion-Patterns/) Instructable by Reza Ali
* [Processing: Reaction Diffusion Halftone patterns](https://vimeo.com/233530691) by Ignazio Lucenti
* [Coral Cup](https://n-e-r-v-o-u-s.com/blog/?p=8222) by Nervous System
* [Reaction Lamps](https://n-e-r-v-o-u-s.com/projects/albums/reaction-products/) by Nervous System
* [Reaction Table](https://n-e-r-v-o-u-s.com/projects/albums/reaction-table/) by Nervous System
* [Reaction-Diffusion Media Wall](http://www.karlsims.com/rd-exhibit.html) by Karl Sims

_Videos:_
* Reaction Diffusion video series for Houdini by Entagma:
  * [Part I: Theory](https://vimeo.com/170073061)
  * [Part II: Implementation](https://vimeo.com/170073069)
  * [Part III: Shaping Growth](https://vimeo.com/170073079)
* [Coding Challenge #13: Reaction Diffusion Algorithm in p5.js](https://www.youtube.com/watch?v=BV9ny785UNc) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_013_ReactionDiffusion) with both p5.js and Processing source code)

<br>

## Math and physics topics
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

_Creative projects:_
* [KnitYak: Custom mathematical knit scarves](https://www.kickstarter.com/projects/fbz/knityak-custom-mathematical-knit-scarves) by Fabienne "fbz" Serriere

_Notable software:_
* [MCell](http://psoup.math.wisc.edu/mcell/) (Mirek's Cellebration)
* [Golly](http://golly.sourceforge.net/)
* [Visions of Chaos](https://www.softology.com.au/voc.htm)

---

<img src="https://upload.wikimedia.org/wikipedia/commons/0/07/CornstarchCymatics_cc.jpg" width="300" align="right">

### Cymatics
_See [Chladni plate](#chladni-plate)_

Study of the visible effects of sound and vibration on physical media. Typically involves the vibration of a plate or membrane onto which fine powder or fluids have been placed, which subsequently arrange themselves into highly symmetrical, complex patterns based on the intensity of displacement of various regions of the vibrating plate. Areas that are moving a lot will "kick" material away from them while areas that are moving very little allow material to settle and accumulate. These areas of relatively little vibration are caused by destructive interference of waves as they propagate across the plate/membrane and become out of phase with one another, creating "dead zones" where these waves cancel each other out.

_Articles:_
* [Cymatics](https://en.wikipedia.org/wiki/Cymatics) on Wikipedia
* [Modal vibrational phenomena](https://en.wikipedia.org/wiki/Normal_mode) on Wikipedia

_Creative projects:_
* [CYMATICS: Science Vs. Music](https://vimeo.com/111593305) by Nigel Stanford
* [Cymatics](https://vimeo.com/74130357) by Susi Sie
* [The Essence of Sound](https://vimeo.com/89491724) by Susi Sie

---

<img src="https://i.imgur.com/iOr8mvo.png" width="300" align="right">

### Delaunay triangulation and Voronoi diagrams
_Delaunay triangulation_ is a way of connecting a set of points to form a network of non-overlapping triangles. One of the key properties of Delaunay triangulations is that the [circumcircles](https://en.wikipedia.org/wiki/Circumscribed_circle) associated with each triangle contains no other points than their three triangle vertices. When extended into 3D, Delaunay triangulation is useful for creating meshes.

_Voronoi diagrams_ are the [dual](https://observablehq.com/@mbostock/the-delaunays-dual) of Delaunay triangulations. This means that once a Delaunay triangulation has been computed for a set of points, a Voronoi diagram can be drawn without any additional data - just draw lines connecting the centers of the circumcircles! 

Voronoi diagrams are very useful for efficiently and organically partitioning (splitting up) both 2D and 3D space. They are especially good for accurately modelling the way soft bodies (like biological cells) get smushed together in constrained environments, like embryonic cells undergoing mitosis.

Voronoi diagrams are often used (perhaps overused) in digital fabrication applications, [especially 3D printing](https://www.google.com/search?q=voronoi+3d+printing&source=lnms&tbm=isch&sa=X&ved=0ahUKEwiQh-npy_HhAhUFSq0KHfBpClQQ_AUIDigB&biw=1920&bih=937), for their characteristic aesthetic style and their ability to reduce material usage while preserving overall form. Given their popularity among amateur 3D printing enthusiasts, this effect is probably best used sparingly in serious applications.

_Articles:_
* [Delaunay triangulation](https://en.wikipedia.org/wiki/Delaunay_triangulation) on Wikipedia
* [Voronoi diagram](https://en.wikipedia.org/wiki/Voronoi_diagram) on Wikipedia

---

<img src="https://vignette.wikia.nocookie.net/golden-ratio/images/f/f1/Fibonacci.png/revision/latest?cb=20140624081839" width="300" align="right">

### Fibonacci sequence
_Related to [Golden ratio](#golden-ratio)_

Sequence of numbers in which each number is the sum of it's two preceding numbers. [Binet's formula](https://en.wikipedia.org/wiki/Fibonacci_number#Binet's_formula) shows that the ratio of two consecutive numbers tends towards the [golden ratio](#golden-ratio) as the sequence progresses. Fibonacci numbers appear unexpectedly often in biology, having been observed in branching of trees, the arrangement of leaves on a stem, the fruit sprouts of a pineapple, the flowering of an artichoke, an uncurling fern and the arrangement of a pine cone's bracts.


<table>
 <thead>
  <tr>
   <th><center>Formula</center></th>
  </tr>
 </thead>
 <tbody>
  <tr> 
   <td>
    <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/3c667d91153450b3a161371582ee8227af85951f"><br>
    <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/0fff1a1716fcc169546079870357f92757ade5fa">
   </td>
  </tr>
 </tbody>
</table>

Sequence begins with:

<img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/ff1558cc1c547dba59ce03cf352c1662b87d10f1">

_Articles:_
* [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_number) on Wikipedia
* [Fibonacci Sequence](https://www.mathsisfun.com/numbers/fibonacci-sequence.html) on Math Is Fun
* [Fibonacci Number](http://mathworld.wolfram.com/FibonacciNumber.html) on Wolfram MathWorld

---

<img src="https://i.kinja-img.com/gawker-media/image/upload/s--L-0h8ess--/c_scale,f_auto,fl_progressive,q_80,w_800/qnkqt6em2iy0rh6drxa0.jpg" width="300" align="right">

### Fluid simulation

Simulates the high complex and dynamic nature of flow of and within fluid volumes using computationally-efficient implementations of the [Navier-Stokes equations](https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations). Can be thought of a 2D or 3D flow field that is constantly changing based on the velocity, viscocity, and density of the fluid at each point in space and its surrounding area. This flow field is made visible through the use of digital "dyes" (colored blobs) that get distributed, diffused, sheared, and blended through the system by the flow forces.

To appear realistic it is necessary for these simulations to have very high fidelity, which introduces significant computational challenges, especially if one wants to run the simulation in real-time. This all but requires the use of GPU technology (see [shaders](#shaders)), making this is a difficult topic to explore independently as a hobbyist. Many VFX, CAD, and game development tools like Blender, Houdini, Unity and Unreal include robust fluid simulation functionality built in, often accessible via APIs and visual UIs.

_Related terms:_
* [Reynolds number](https://en.wikipedia.org/wiki/Reynolds_number) (Re) - dimensionless quantity used to predict fluid flow patterns. [Laminar](https://en.wikipedia.org/wiki/Laminar_flow) (smooth) flow occurs at low Re, while [turbulent](https://en.wikipedia.org/wiki/Turbulence) flow occurs at high Re.
* [Navier-Stokes equations](https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations) on Wikipedia
* [Lattice Boltzmann methods](https://en.wikipedia.org/wiki/Lattice_Boltzmann_methods) (LBM) on Wikipedia

_Articles:_
* [Computational fluid dynamics](https://en.wikipedia.org/wiki/Computational_fluid_dynamics) (CFD) on Wikipedia
* [Fluid Simulation for Dummies](https://mikeash.com/pyblog/fluid-simulation-for-dummies.html) by Mike Ash
* [Real-Time Fluid Dynamics for Games](http://www.dgp.toronto.edu/people/stam/reality/Research/pdf/GDC03.pdf) (PDF) by Jos Stam
* [Chapter 38. Fast Fluid Dynamics Simulation on the GPU](http://developer.download.nvidia.com/books/HTML/gpugems/gpugems_ch38.html) from GPU Gems book

_Code projects:_
* [Lily Pad](https://github.com/weymouth/lily-pad) by Dr. Gabriel David Weymouth
* [MSAFluid](https://www.memo.tv/msafluid/) by Memo Akten

_Videos:_
* [Coding Challenge #132: Fluid Simulation](https://www.youtube.com/watch?v=alhpH6ECFvQ) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_132_FluidSimulation) with source code for p5.js and Processing)
* [Why Laminar Flow is AWESOME - Smarter Every Day 208](https://www.youtube.com/watch?v=y7Hyc3MRKno&feature=youtu.be) by Smarter Every Day

---

<img src="https://i.stack.imgur.com/cfnQu.gif" width="300" align="right">

### Fourier series
Series of sinusoidal wave functions that get added together to generate a different, more complex function. In the context of morphogenesis (form generation), any line drawing can be "deconstructed" into a series of arc segments which can in turn be represented by a series of circles whose radii and rotation speeds correspond to the radii and lengths of the arc segments.

Fourier series and Fourier transforms are deeply mathematical topics with applications and research far beyond the scope of this resource list. They are extremely useful in the field of digital signal processing for noise reduction, compression, audio analysis, and so much more. A very well-known algorithm known as the [fast Fourier transform (FFT)](https://en.wikipedia.org/wiki/Fast_Fourier_transform) enables extraction of waveforms from music for the purposes of audio visualization.

_Articles:_
* [Fourier series](https://en.wikipedia.org/wiki/Fourier_series) on Wikipedia
* [Fourier Series](http://mathworld.wolfram.com/FourierSeries.html) on Wolfram MathWorld
* [Fourier Series](https://www.mathsisfun.com/calculus/fourier-series.html) on Math Is Fun

_Videos:_
* [What is a Fourier Series? (Explained by drawing circles)](https://www.youtube.com/watch?v=ds0cmAV-Yek&vl=en) by Smarter Every Day
* [But what is the Fourier Transform? A visual introduction](https://www.youtube.com/watch?v=spUNpyF58BY) by 3Blue1Brown
* [Coding Challenge #125: Fourier Series](https://www.youtube.com/watch?v=Mm2eYfj0SgA) by Daniel Shiffman
* [Coding Challenge #130.1: Drawing with Fourier Transform and Epicycles](https://www.youtube.com/watch?v=MY4luNgGfms) by Daniel Shiffman
* [Coding Challenge #130.2: Fourier Transform User Drawing](https://www.youtube.com/watch?v=n9nfTxp_APM) by Daniel Shiffman
* [Coding Challenge #130.3: Fourier Transform Drawing with Complex Number Input](https://www.youtube.com/watch?v=7_vKzcgpfvU) by Daniel Shiffman

---

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Mandel_zoom_08_satellite_antenna.jpg/320px-Mandel_zoom_08_satellite_antenna.jpg" width="300" align="right">

### Fractals
Infinitely complex patterns generated via [recursion](#recursion) that are self-similar across all scales. Thought to be found in abundance in nature, though "true" (infinite) fractals are not possible because nature uses physical matter, which has particular structures at the microscopic and smaller scales (molecules, atoms, elementary particles, etc).

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

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Golden_Angle.svg/479px-Golden_Angle.svg.png" width="300" align="right">

### Golden angle
_Related to the [golden ratio](#golden-ratio) and [phyllotaxis](#phyllotaxis)._

Radial version of the [golden ratio](#golden-ratio). It is the smaller of the two angles created by sectioning the circumference of a circle according to the golden ratio; that is, into two arcs such that the ratio of the length of the smaller arc to the length of the larger arc is the same as the ratio of the length of the larger arc to the full circumference of the circle.

In degrees the angle is approximately `137.5077640500 ...`, or just `137.5` for brevity.

_Articles:_
* [Golden angle](https://en.wikipedia.org/wiki/Golden_angle) on Wikipedia
* [The Golden Angle](http://gofiguremath.org/natures-favorite-math/the-golden-ratio/the-golden-angle/) by Go Figure

_Creative projects:_
* [Golden Angle](http://www.johnedmark.com/phi) sculpture series by John Edmark

---

<img src="https://betterexplained.com/wp-content/uploads/2017/04/golden_ratio_example.png" width="300" align="right">

### Golden ratio
_Related to the [Fibonacci sequence](#fibonacci-sequence)._

Also expressed as the Greek letter _phi_ (`φ`), this irrational number pops up when the ratio of two numbers is the same as the ratio of their sum to the largest of the two numbers. It has been observed in many fields of the natural sciences at every scale and is has become associated with aesthetic beauty, giving it a nearly mythic reputation for some. 

_Expressed algebraicly:_

<img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/d4010f92e33cc559bc8d7f24b4ed017273a0628d">

_Expressed as line segments:_

<img src="https://upload.wikimedia.org/wikipedia/commons/4/44/Golden_ratio_line.svg">

_Articles:_
* [Golden ratio](https://en.wikipedia.org/wiki/Golden_ratio) on Wikipedia
* [Golden Ratio](https://www.mathsisfun.com/numbers/golden-ratio.html) on Math is Fun
* [Golden Ratio](http://mathworld.wolfram.com/GoldenRatio.html) on Wolfram MathWorld

---

<img src="https://upload.wikimedia.org/wikipedia/commons/c/cb/5R_robot.gif" width="300" align="right">

### Inverse and forward kinematics
Equations used to calaculate the positions of a series of rigidly-linked segments (called the _kinematic chain_) based on the location of the end effector, usually located at the tip of the last segment. Useful for robotic systems like drawing machines, robot arms, and more.

**Inverse** kinematics calculate the angles of each linked segment given the desired location of the end effector. Will give you the angles of each segment, which can in turn be converted into motor positions for a robot.

**Forward** kinematics calculate the location of the end effector given the angles and lengths of each linked segment. 

_Articles:_
* [Kinematics](https://en.wikipedia.org/wiki/Kinematics) on Wikipedia
* [Inverse kinematics](https://en.wikipedia.org/wiki/Inverse_kinematics) on Wikipedia
* [Forward kinematics](https://en.wikipedia.org/wiki/Forward_kinematics) on Wikipedia

_Videos:_
* [Coding Challenge #64.1: Forward Kinematics](https://www.youtube.com/watch?v=xXjRlEr7AGk) by Daniel Shiffman
* [Coding Challenge #64.2: Inverse Kinematics](https://www.youtube.com/watch?v=hbgDqyy8bIw) b Daniel Shiffman
* [Coding Challenge #64.3: Inverse Kinematics - Fixed Point](https://www.youtube.com/watch?v=RTc6i-7N3ms) by Daniel Shiffman
* [Coding Challenge #64.4: Inverse Kinematics - Multiple](https://www.youtube.com/watch?v=10st01Z0jxc) by Daniel Shiffman

---

### Laplace transform

```
TODO
```
---

<img src="https://thumbs.gfycat.com/AngelicDismalAmazonparrot-max-1mb.gif" width="300" align="right">

### Lissajous curves

Also known as Bowditch curves, these figures plot the trajectories of a point as it follows the path of two simultaneous sinusoidal motions.

Can be created using various physical systems including [oscilloscopes](https://www.youtube.com/watch?v=t6nGiBzGLD8), [harmonographs](https://en.wikipedia.org/wiki/Harmonograph), and more.

_Equations:_

<img src="https://www.mathcurve.com/courbes2d.gb/lissajous/imageGSM.JPG"><br>
<img src="https://www.mathcurve.com/courbes2d.gb/lissajous/imageRGH.JPG">

_Articles:_
* [Lissajous curve](https://en.wikipedia.org/wiki/Lissajous_curve) on Wikipedia
* [Lissajous curve](https://www.mathcurve.com/courbes2d.gb/lissajous/lissajous.shtml) from MathCurve
* [Lissajous Curves](http://datagenetics.com/blog/april22015/index.html) from DataGenetics

_Videos:_
* [Coding Challenge #116: Lissajous Curve Table](https://www.youtube.com/watch?v=--6eyLO78CY) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_116_Lissajous) with source code for p5.js and Processing)
* [#48: Basics of Lissajous Patterns on an Oscilloscope](https://www.youtube.com/watch?v=t6nGiBzGLD8) by w2aew

---

<img src="https://www.researchgate.net/profile/Christoph_Kinkeldey/publication/237408245/figure/fig2/AS:299459092205573@1448408019217/Medial-axis-of-a-body-in-2D-Euklidian-space-Wolter-2001.png" width="300" align="right">

### Medial axis
The medial axis is sort of like the "skeleton" of a shape. It consists of a set of lines and curves upon which every point is equidistant between at least one closest point on the shape's boundary. In 2D this skeleton can also be thought of as a set of lines/curves whose points are the centers of circles that are tangent to at least two points on the shape's boundary.

Has applications in computer vision, pose estimation, 2D/3D character rigging, architecture, BIM (escape route optimization), and more.

_Related terms:_
* Medial-axis transform - medial axis together with the associated radius function of the maximally inscribed discs. Can be used to reconstruct a shape.
* [Topological Skeleton](https://en.wikipedia.org/wiki/Topological_skeleton)
* [Straight skeleton](https://en.wikipedia.org/wiki/Straight_skeleton) - similar to medial, except always is made up of straight line segments whereas medial axis may contain curves.
* [Scale Axis Transform](http://www.balintmiklos.com/scale-axis/theory_socg_2009.html) - generalization of medial axis transform

_Articles:_
* [Medial axis](https://en.wikipedia.org/wiki/Medial_axis) on Wikipedia
* ["A transformation for extracting new descriptors of shape"](http://pageperso.lif.univ-mrs.fr/~edouard.thiel/rech/1967-blum.pdf) by Henry Blum

---

### Minimal surface

```
TODO
```

_Articles:_
* [Minimal surface](https://en.wikipedia.org/wiki/Minimal_surface)

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

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Aloe_polyphylla_1.jpg/564px-Aloe_polyphylla_1.jpg" width="300" align="right">

### Phyllotaxis
_Related topics include the [golden ratio](#golden-ratio), the [golden angle](#golden-angle), and the [Fibonacci sequence](#fibonacci-sequence)._

Refers to the arrangement (_taxis_) of leaves (_phyllo_) on a plant stem. Also can refer to seed arrangements and succulent geometry.

_Types:_
* Opposite - two leaves arise from the stem at the same level on opposite sides of the stem
* Alternate - each leaf arises at a different point (node) on the stem
* [Whorled](https://en.wikipedia.org/wiki/Whorl_(botany)) - arrangement of leaves that radiate from a single point and surround or wrap around the stem, as seen in the thumbnail for this section.
* Distichous - special case of either opposite or alternate leaf arrangement where the leaves on a stem are arranged in two vertical columns on opposite sides of the stem
* Decussate - occurs when successsive pairs of leaves arranged in the opposite pattern are 90 degrees apart, as in [Aizoaceae](https://en.wikipedia.org/wiki/Aizoaceae) family

_Articles:_
* [Phyllotaxis](https://en.wikipedia.org/wiki/Phyllotaxis) on Wikipedia
* [Chapter 4: Phyllotaxis](http://algorithmicbotany.org/papers/abop/abop-ch4.pdf) from Algorithmic Botany book
* [Phyllotaxis](http://mathworld.wolfram.com/Phyllotaxis.html) on Wolfram MathWorld

_Code projects:_
* [ofxPhyllotaxis](https://github.com/edap/ofxPhyllotaxis) by Davide Prati (edap)

_Videos:_
* [Coding Challenge #30: Phyllotaxis](https://www.youtube.com/watch?v=KWoJgHFYWxY) by Daniel Shiffman

---

### Spherical harmonics

```
TODO
```

_Articles:_
* [Spherical harmonics](https://en.wikipedia.org/wiki/Spherical_harmonics) on Wikipedia
* [Spherical Harmonics](http://paulbourke.net/geometry/sphericalh/) by Paul Bourke

---

<img src="https://upload.wikimedia.org/wikipedia/commons/4/4a/Attractor_Poisson_Saturne.jpg" width="300" align="right">

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
* [Superellipse](http://mathworld.wolfram.com/Superellipse.html) on Wolfram MathWorld
* [Supershapes (Superformula)](http://paulbourke.net/geometry/supershape/) by Paul Bourke

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

_Articles:_
* [Superformula](https://en.wikipedia.org/wiki/Superformula) on Wikipedia
* [Supershapes / Superformula](http://paulbourke.net/geometry/supershape/) by Paul Bourke

_Code projects:_
* [SuperformulaSVG-for-web](https://github.com/jasonwebb/SuperformulaSVG-for-web) by Jason Webb (Javascript, p5.js)
* [SuperformulaSVG](https://github.com/jasonwebb/SuperformulaSVG) by Jason Webb (Processing)
* [Visualize: Superformula](http://formandcode.com/code-examples/visualize-superformula) from FORM+CODE book
* [glsl-superformula](https://github.com/Softwave/glsl-superformula) by JC Leyba (Software)
* [supershape.js](https://github.com/ahoiin/supershape.js) by Sebastian Sadowski (ahoiin)

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

<br>

## Lab experiments

<img src="https://live.staticflickr.com/3626/3572095252_a43ca95002_b.jpg" width="300" align="right">

### Belousov–Zhabotinsky reaction

```
TODO
```

_Articles:_
* [Belousov–Zhabotinsky reaction](https://en.wikipedia.org/wiki/Belousov%E2%80%93Zhabotinsky_reaction) on Wikipedia
* [Belousov-Zhabotinsky reaction](http://www.scholarpedia.org/article/Belousov-Zhabotinsky_reaction) on Scholarpedia

_Code projects:_
* [Simulating the Belousov-Zhabotinsky reaction](https://scipython.com/blog/simulating-the-belousov-zhabotinsky-reaction/) (Python) by Christian Hill

_Videos:_
* [Belousov-Zhabotinsky Reaction](https://www.youtube.com/watch?v=IBa4kgXI4Cg) by nater06

---

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a1/Quadratic_Chladni_plate.JPG/760px-Quadratic_Chladni_plate.JPG" width="300" align="right">

### Chladni plate

```
TODO
```

---

<img src="http://n-e-r-v-o-u-s.com/blog/wp-content/uploads/2011/04/5597278928_fed4566d5b_b.jpg" width="300" align="right" alt="Hele-Shaw cell experiment by Nervous System">

### Hele-Shaw cell experiment

```
TODO
```

_Articles:_
* [Hele-Shaw flow](https://en.wikipedia.org/wiki/Hele-Shaw_flow) on Wikipedia

_Videos:_
* [Hele-Shaw cell experiments](https://vimeo.com/22212386) by Nervous System
* [Hele Shaw Cell](https://www.youtube.com/watch?v=yys3q_XBRI4) using ferrofluid and a magnet by manf1234
* [Viscous Fingering in Multiport Hele Shaw Cell for Controlled Shaping of Fluids](https://www.youtube.com/watch?v=wegYlxGXhW8) by Tanveer ul Islam and Prasanna S. Gandhi

_Images:_
* [Schlieren Imaging of Viscous Fingering and Buoyancy Driven Convection](https://art-csep.cnsi.ucsb.edu/gallery/schlieren-imaging-viscous-fingering-and-buoyancy-driven-convection) by Simone Stewart

---

<img src="https://66.media.tumblr.com/5870353e177a43d3c6499cfbd952acb2/tumblr_nom1mwy8zg1qabnxjo1_1280.gif" width="300" align="right">

### Schlieren imaging

```
TODO
```

_Articles:_
* [Schlieren imaging](https://en.wikipedia.org/wiki/Schlieren_imaging) on Wikipedia

<br>

## Useful code patterns and techniques

### Agent-based modelling

```
TODO
```

_Notables systems:_
* [Boids](https://en.wikipedia.org/wiki/Boids)

_Articles:_
* [Agent-based model](https://en.wikipedia.org/wiki/Agent-based_model) on Wikipedia

---

<img src="https://cdn-images-1.medium.com/max/800/1*CHhG6Ea1664UrKwaJhiDTQ.png" width="300" align="right">

### Collision detection
Computational methods for determining when two or more shapes are intersecting either statically (right now) or predictively (in the future). In technical terms, _a posterior_ and _a priori_ respectively. Detecting and reacting to collisions is extremely important in videos games and physical simulations, and takes quite a lot of brains and computational muscle to do effectively in real-time, especially in large-scale systems.

Building your own collision detection code is a fun and educational exercise, but is so complex and difficult to achieve in practice that it is generally a good idea to use an establisihed physics library or VFX/modelling application for performance. See the [Physics engine](#physics-engine) and [Tools](#tools) sections for options.

_Relevant topics:_
* Broad phase - class of algorithms that detect pairs of _potentially_ colliding shapes using fast but approximate methods, such as:
  * [Axis-aligned bounding box](https://en.wikipedia.org/wiki/Minimum_bounding_box#Axis-aligned_minimum_bounding_box) (AABB)
  * [Sort and sweep](https://en.wikipedia.org/wiki/Sweep_and_prune) (a.k.a. sweep and prune)
  * [Bounding volume hierarchy](https://en.wikipedia.org/wiki/Bounding_volume_hierarchy) (BVH)
* Narrow phase - class of algorithms that determine if two shapes are definately intersecting or not, and by how much.
  * [Separating axis theorem](https://gamedevelopment.tutsplus.com/tutorials/collision-detection-using-the-separating-axis-theorem--gamedev-169) (SAT)
  * [Gilbert-Johnson-Keerthi](https://en.wikipedia.org/wiki/Gilbert%E2%80%93Johnson%E2%80%93Keerthi_distance_algorithm) (GJK) algorithm
  * Expanding Polytope Algorithm (EPA)

_Articles:_
* [Collision detection](https://en.wikipedia.org/wiki/Collision_detection) on Wikipedia
* [Video Game Physics Tutorial - Part II: Collision Detection for Solid Objects](https://www.toptal.com/game/video-game-physics-part-ii-collision-detection-for-solid-objects) by Nilson Souto
* [Let's talk about broad phase](http://podgorskiy.com/spblog/40/lets-talk-about-broad-phase) by Stanislav Pidhorskyi

_Books:_
* [Real-Time Collision Detection](https://smile.amazon.com/exec/obidos/tg/detail/-/1558607323/realtimecolli-20/?sa-no-redirect=1) by Christer Ericson

---

<img src="https://www.visgraf.impa.br/Courses/ip00/proj/Dithering1/image/lena%20ordered.gif" width="300" align="right">

### Dithering
Creates the illusion of depth in an image using a limited color palette, most commonly by varying the spacing or sizes of solid, single-color dots or lines. Some techniques (like [halftones](https://en.wikipedia.org/wiki/Halftone)) even predate modern digital technologies because of their usefulness in traditional printmaking and engraving processes. There are even relevant techniques in the fields of painting and drawing; see [stippling](https://en.wikipedia.org/wiki/Stippling) and [pointillism](https://en.wikipedia.org/wiki/Pointillism)!

Useful for realizing grayscale images with various digital fabrication equipment like laser cutters, pen plotters, CNC routers/mills, and more.

_Types of dithering:_
* Threshold (a.k.a average)
* Random
* Patterned
* Ordered
  * Halftone ⭐
  * Bayer matrix
  * Blue noise matrix
* Error-diffusion
  * Floyd-Steinberg ⭐
  * Minimized average error
  * Stucki
  * Burkes
  * Sierra
  * Two-row Sierra
  * Filter Lite
  * Atkinson
  * Gradient-based error-diffusion

_Articles:_
* [Dither](https://en.wikipedia.org/wiki/Dither#Digital_photography_and_image_processing) on Wikipedia

_Code projects:_
* [Coding Challenge #90: Floyd-Steinberg Dithering](https://www.youtube.com/watch?v=0L2n8Tg2FwI) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_090_dithering) with source code for p5.js and Processing)
* [Atkinson Dithering, Live in Processing](https://www.evilmadscientist.com/2012/dithering/) by Windell Oskay of Evil Mad Scientist Laboratories
* [#dithering-algorithms](https://github.com/topics/dithering-algorithms) on Github
* [Digital Halftoning](https://engineering.purdue.edu/~bouman/ece637/notes/pdf/Halftoning.pdf) by C. A. Bouman
* [Color Quantization and Dithering](http://www.imagemagick.org/Usage/quantize/) reference page for ImageMagick v6

---

<img src="http://www.bushwalking101.org/wp-content/uploads/2016/09/elevation.png" width="300" align="right">

### Marching squares
Method of generating contours for a 2D scalar field (a grid of individual numerical values), like turning elevation data into a banded topographical map. The scalar values get associated with vertices of the 2D grid, then lines are drawn across each cell in different ways based on the values of their four corner vertices. 

There is only a finite number of lines possible, so they can be precomputed into a lookup table and referenced quickly later for faster performance. These lines can also be linearly interpolated to smoothly transition from cell to cell, resulting in very realistic blobby / fluid structures.

_Key terms:_
* Isoline - contour line tracing a single data level, or _isovalue_.
* Isoband - filled area between isolines.

_Illustration of algorithm:_

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/00/Marching_squares_algorithm.svg/710px-Marching_squares_algorithm.svg.png" width="500">

_Articles:_
* [Marching squares](https://en.wikipedia.org/wiki/Marching_squares) on Wikipedia
* [Metaballs and Marching Squares](http://jamie-wong.com/2014/08/19/metaballs-and-marching-squares/) by Jamie Wong

_Code projects:_
* [d3-contour](https://github.com/d3/d3-contour) - D3.js library

_Videos:_
* [Marching Squares](https://unity3d.com/learn/tutorials/projects/procedural-cave-generation-tutorial/marching-squares) for procedural cave generation in Unity by Sebastian Lague

---

<img src="https://i.ytimg.com/vi/LC0IbOZ0jkw/maxresdefault.jpg" width="300" align="right">

### Marching cubes
3D version of [marching squares](#marching-squares). Whereas marching _squares_ uses lines and cells to trace the contours of a 2D scalar field, marching _cubes_ uses polygons and voxels to trace the contours of a 3D scalar field, resulting in a mesh.

```
TODO: add note on dual marching cubes
```

_Key terms:_
* Isosurface - surface that represents points of a constant value within a volume of space

_Articles:_
* [Marching cubes](https://en.wikipedia.org/wiki/Marching_cubes) on Wikipedia
* [Polygonising a scalar field](http://paulbourke.net/geometry/polygonise/) by Paul Bourke
* [Voxel to Mesh Conversion: Marching Cube Algorithm](https://medium.com/zeg-ai/voxel-to-mesh-conversion-marching-cube-algorithm-43dbb0801359) by Smile Sikand

---

### Metaballs
_Related to [marching squares](#marching-squares) (2D) and [marching cubes](#marching-cubes) (3D)_

```
TODO
```

_Articles:_
* [Metaballs](https://en.wikipedia.org/wiki/Metaballs) on Wikipedia

---

<img src="https://answers.unity.com/storage/temp/97016-perlin2.png" width="300" align="right">

### Noise
In the context of computer graphics, refers to pseudo-random functions useful for creating natural-looking textures and patterns. Often used to procedurally generate organic surface textures (bark, waves, rocks, etc) and to organically distribute objects across surfaces (like grass or barnacles). 

Useful for adding fine details and smooth asymmetry to otherwise pristine objects - use it in displacement maps for subtle natural features. 

Also helpful for creating looping animations because reproducable results can be achieved when using the same function inputs. Just iterate through a series of cyclical values (perhaps even based on frame count) and you'll end up with smoothly transitioning noise that can be mixed in with geometry, colors, and transformations that continuously loop.

The `noise()` function in many creative coding frameworks usually makes use of Perlin noise.

* [Gradient noise](https://en.wikipedia.org/wiki/Gradient_noise) - created by interpolation of a lattice of pseudorandom gradients
  * [Perlin noise](https://en.wikipedia.org/wiki/Perlin_noise) ⭐ - extremely influential type of gradient noise developed by Ken Perlin in 1983
* [Simplex noise](https://en.wikipedia.org/wiki/Simplex_noise) - method for constructing an n-dimensional noise function comparable to Perlin noise
* [Simuation noise](https://en.wikipedia.org/wiki/Simulation_noise) - function that creates a divergence-free field
* [Value noise](https://en.wikipedia.org/wiki/Value_noise) - created by interpolation of a lattice of pseudorandom values; differs from gradient noise
* [Wavelet noise](https://en.wikipedia.org/wiki/Wavelet_noise) - alternative to Perlin noise which reduces problems of aliasing and detail loss
* [Worley noise](https://en.wikipedia.org/wiki/Worley_noise) - noise function introduced by Steven Worley in 1996

_Articles:_
* [Noise](https://thebookofshaders.com/11/) chapter in The Book of Shaders by Patricio Gonzalez Vivo & Jen Lowe

_Videos:_
* [Coding Challenge #11: 3D Terrain Generation with Perlin Noise in Processing](https://www.youtube.com/watch?v=IKB1hWWedMk) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_011_PerlinNoiseTerrain) with source code for p5.js and Processing)
* [Coding Challenge #136.1: Polar Perlin Noise Loops](https://www.youtube.com/watch?v=ZI1dmHv3MeM) by Daniel Shiffman ([Github repo](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_136_Polar_Noise_Loop_1) [[2]](https://github.com/CodingTrain/website/tree/master/CodingChallenges/CC_136_Polar_Noise_Loop_2) with source code for p5.js and Processing)

```
TODO: add note on curl noise
```

---

<img src="https://static.skillshare.com/uploads/video/thumbnails/c1c3da12ee479172705d9967ec9dca78/original" width="300" align="right">

### Particle system
Collection of independent objects (often points, shapes, images/sprites/textures, or meshes) called _particles_ that are manipulated using dynamic forces and constraints to simulate a wide variety of natural phenomenon like fire, smoke/fog/clouds, fluids, bubbles, and so much more. Often combined with clever visual effects like transparency, blending, and light emission to create the appearance of a coherent but ever-changing entity.

Particle systems are most useful when they can handle large quantities of particles, which means that performance and smart memory management is very important. Like [collision detection](#collision-detection), building your own particle system can be fun and educational, but if you need to achieve something complex at a large scale and/or with high framerates then it's definitely a good idea to leverage dedicated libraries and tools. Many [physics engines](#physics-engine) come with well-made particle systems out of necessity so be sure to consider them even if you don't need all the fun physics functionality.

_Articles:_
* [Particle system](https://en.wikipedia.org/wiki/Particle_system) on Wikipedia
* [Intro to particle systems](https://www.khanacademy.org/computing/computer-programming/programming-natural-simulations/programming-particle-systems/a/intro-to-particle-systems) lesson on Khan Academy
* [Chapter 4. Particle Systems](https://natureofcode.com/book/chapter-4-particle-systems/) from Nature of Code

_Notable software:_
* [Unity's VFX Graph](https://unity.com/visual-effect-graph)
* [Blender's Particle System](https://docs.blender.org/manual/en/latest/physics/particles/index.html)

---

<img src="http://html5gamedevelopment.com/wp-content/uploads/2017/03/2017-03-29-12_59_02-Pyramid-Planck.js.png" width="300" align="right">

### Physics engine
_Related topics include [collision detection](#collision-detection) and [particle systems](#particle-system)_

Simulates the movements and reactions of objects using real-world concepts like mass, velocity, constraints, and forces (like drag, gravity, and friction). Makes use of extremely optimized algorithms for collision detection, physics calculations, geometry management, and more.

_Articles:_
* [Physics engine](https://en.wikipedia.org/wiki/Physics_engine) on Wikipedia
* [Chapter 5. Physics Libraries](https://natureofcode.com/book/chapter-5-physics-libraries/) from Daniel Shiffman's Nature of Code book
* [How to Create a Custom 2D Physics Engine: The Basics and Impulse Resolution](https://gamedevelopment.tutsplus.com/tutorials/how-to-create-a-custom-2d-physics-engine-the-basics-and-impulse-resolution--gamedev-6331) by Randy Gaul

_Notable open-source libraries:_
* [Box2D](https://github.com/erincatto/Box2D) (C++)
  * [LiquidFun](http://google.github.io/liquidfun/) (C++) - adds rigid-body and fluid dynamics on top of Box2D
  * [box2d.js](https://github.com/kripken/box2d.js) (JavaScript via Emscripten)
  * [Planck.js](https://github.com/shakiba/planck.js) (JavaScript, manually ported)
* [Bullet](https://github.com/bulletphysics/bullet3) (C++)
  * [ammo.js](https://github.com/kripken/ammo.js/) (direct JavaScript port using Emscripten) 
* [Matter.js](http://brm.io/matter-js/) (JavaScript)
* [dyn4j](http://www.dyn4j.org/) (Java)
* [cannon.js](http://schteppe.github.io/cannon.js/) (JavaScript)
* [p2.js](https://github.com/schteppe/p2.js) (JavaScript)
* [ReactPhysics3D](https://www.reactphysics3d.com/) (C++)
* [Chrono](http://projectchrono.org/) (C++)
* [Open Dynamics Engine (ODE)](https://www.ode.org/) (C++)

_Commercial libraries:_
* [PhysX](https://en.wikipedia.org/wiki/PhysX) by Nvidia. Integrated into both Unity and Unreal. Technically open-source now, but oriented more towards commercial/industry applications.
* [Havok](https://www.havok.com/products/havok-physics/)

If you're looking to do physical-based simulations, also take a look at game development and VFX environments like [Unity](https://unity3d.com/learn/tutorials/s/physics?_ga=2.158332858.1012620598.1557960859-2002016059.1556146318), [Unreal](https://docs.unrealengine.com/en-us/Engine/Physics), and [Houdini](https://www.sidefx.com/products/houdini/) for their built-in physics engines.

---

### Recursion
_See [recursion](#recursion)._

```
TODO
```

_Articles:_
* [Recursion](https://en.wikipedia.org/wiki/Recursion) on Wikipedia

---

### Shaders
Shaders are programs that are run on the GPU when processing a certain unit of rendering, usually vertices or pixels/fragments; they allow rendering programmers to manipulate their rendering output in any way they see fit.

While shaders, as the name implies, were originally conceived to allow different kinds of lighting/shading calculations, today they're used for a variety of things from lighting calculation through stylized rendering to 2D compositing or post-processing, and even complex geometry manipulations and particle effects.

_Types of shaders:_
* Vertex
* Fragment
* Compute

_Key terms:_
* [HLSL (High-Level Shading Language)](https://en.wikipedia.org/wiki/High-Level_Shading_Language) - shading language used by DirectX
* [GLSL (OpenGL Shading Language)](https://en.wikipedia.org/wiki/OpenGL_Shading_Language) - shading language used by OpenGL
* [GPGPU (General-purpose computing on GPUs)](https://en.wikipedia.org/wiki/General-purpose_computing_on_graphics_processing_units)
* [CUDA](https://en.wikipedia.org/wiki/CUDA) - parallel computing API that makes it easier to use GPGPU for complicated tasks
* [Cg](https://en.wikipedia.org/wiki/Cg_(programming_language)) - shading language developed by Nvidia in close collaboration with Microsoft
* [Shading language](https://en.wikipedia.org/wiki/Shading_language)

_Articles:_
* [The Book of Shaders](https://thebookofshaders.com/) by Patricio Gonzalez Vivo and Jen Lowe
* [Shaders](https://learnopengl.com/Getting-started/Shaders) by Learn OpenGL
* [GLSL Shaders](https://developer.mozilla.org/en-US/docs/Games/Techniques/3D_on_the_web/GLSL_Shaders) on MDN web docs
* [Shaders](https://processing.org/tutorials/pshader/) (Processing) tutorial by Andres Colubi
* [Introducing Shaders](https://openframeworks.cc/ofBook/chapters/shaders.html) (openFrameworks) by Lucasz Karluk, Joshua Noble, Jordi Puig
* [Shader modules](https://vulkan-tutorial.com/Drawing_a_triangle/Graphics_pipeline_basics/Shader_modules) (Vulkan)

_Software:_
* [RenderMonkey](https://gpuopen.com/archive/gamescgi/rendermonkey-toolsuite/)
* [Bonzomatic](https://github.com/Gargaj/Bonzomatic)
* [Shadertoy](https://www.shadertoy.com/)

_Videos:_
* [Shader Coding seminar at Revision 2019](https://www.youtube.com/watch?v=uFFR31t1WMM)

---

### Signed distance function (SDFs)
A signed distance function is a function that returns the distance of a point in space to a mathematically/algorithmically defined surface. This allows algorithms like raymarching to efficiently render complex 3D surfaces in 2D.

SDFs are increasingly commonly used in computer art, where defining an SDF that describes a large 3D scene entirely in a single pixel shader allows the code to be ran entirely on the GPU.

_Articles:_
* [Signed distance function](https://en.wikipedia.org/wiki/Signed_distance_function) on Wikipedia
* [Distance functions](http://iquilezles.org/www/articles/distfunctions/distfunctions.htm)  (GLSL)

_Notable open-source libraries:_
* [hg_sdf](http://mercury.sexy/hg_sdf/) (GLSL)

_Videos:_
* [How to Create Content with Signed Distance Functions by Johann Korndörfer](https://www.youtube.com/watch?v=s8nFqwOho-s)

---

<img src="https://upload.wikimedia.org/wikipedia/commons/8/8b/Point_quadtree.svg" width="300" align="right">

### Spatial index
Data structure (most commonly a binary tree) that enables fast and efficient storage, manipulation, and querying of large amounts of spatial data (points in space). Commonly used by [particle systems](#particle-system).

_Common types:_
* [Quadtree](https://en.wikipedia.org/wiki/Quadtree) - each node has exactly four children
* [Octree](https://en.wikipedia.org/wiki/Octree) - each node has exactly eight children
* [k-d tree](https://en.wikipedia.org/wiki/K-d_tree)
* [R-tree](https://en.wikipedia.org/wiki/R-tree)

_Related topics:_
* [k-nearest neighbhor (knn) search](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm)
* [Spatial database](https://en.wikipedia.org/wiki/Spatial_database) on Wikipedia
* [Binary space partitioning](https://en.wikipedia.org/wiki/Binary_space_partitioning) on Wikipedia

_Articles:_
* [Spatial index](https://en.wikipedia.org/wiki/Spatial_database#Spatial_index) section on Wikipedia article for Spatial database

_Videos:_
* Coding Challenge #98: [Part 1](https://www.youtube.com/watch?v=OJxEcs0w_kE), [Part 2](https://www.youtube.com/watch?v=QQx_NmCIuCY), [Part 3](https://www.youtube.com/watch?v=z0YFFg_nBjw) by Daniel Shiffman

---

<img src="https://camo.githubusercontent.com/dc39c61e02aa67abd0f923628cf241120d14f517/687474703a2f2f692e696d6775722e636f6d2f734e75425653722e676966" width="300" align="right">

### Wave Function Collapse (WFC)
Method of procedurally generating textures and tilemaps that are similar to a single source image using ideas from quantum mechanics.

```
TODO - add description of algorithm
```

_Articles:_
* Original [WaveFunctionCollapse Github repo](https://github.com/mxgmn/WaveFunctionCollapse) by Maxim Gumin (mxgmn)
* [Generating Worlds With Wave Function Collapse](http://www.procjam.com/tutorials/wfc/) by Joseph Parker
* [Doodle Insights #19: Logic Data Generation (feat. WFC made easy)](https://trasevol.dog/2017/09/01/di19/) by Rémy Devaux (TRASEVOL_DOG)

<br>

## Books and publications
### Books
* [On Growth and Form](https://smile.amazon.com/Growth-Form-Complete-Revised/dp/0486671356/) by D'Arcy Wentworth Thompson
* Nature's Patterns: A Tapestry in Three Parts by Philip Ball
  * [Flow](https://smile.amazon.com/Flow-Natures-Patterns-Tapestry-Three/dp/0199604878/)
  * [Branches](https://smile.amazon.com/Branches-Natures-Patterns-Tapestry-Three/dp/0199604886/)
  * [Shapes](https://smile.amazon.com/Shapes-Natures-Patterns-Tapestry-Three/dp/0199237964/)
* [Fractal Concepts in Surface Growth](https://smile.amazon.com/Fractal-Concepts-Surface-Albert-Laszlo-Barabasi/dp/0521483182) by Albert-László Barabási
* [Fractal Growth Phenomena](https://smile.amazon.com/gp/product/9810206690/) by Tamas Vicsek

### Publications
* [Zygote Quarterly](https://zqjournal.org/)

<br>

## Software

### Tools
<table>
  <thead>
    <tr>
      <th>Application</th>
      <th width="50%">Description</th>
      <th>Cost</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top"><a href="https://www.sidefx.com/products/houdini/" target="_blank">Houdini</a></td>
      <td valign="top">Industry-level procedural VFX application with graphical node-based workflow. Excellent for creating high-quality renderings and animations based on generative algorithms.</td>
      <td valign="top">
        <ul>
          <li>Free with watermarked renders for non-commercial users (Apprentice)</li>
          <li>$269 for no watermarks for commercial <$100k annual profit (Indie)</li>
          <li>Thousands for commercial users, with complex pricing model</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td valign="top"><a href="https://www.rhino3d.com/" target="_blank">Rhino</a></td>
      <td valign="top">NURBS-based CAD program popular with architects and designers.</td>
      <td valign="top">
        <ul>
          <li>Rhino 6 for Win - $995</li>
          <li>Rhino 5 for Mac - $695</li>
          <li>$195 for students (both platforms)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="3">
        <details>
          <summary>List of useful Rhino plugins</summary>
          <p>
            <ul>
              <li><a href="https://www.grasshopper3d.com/" target="_blank">Grasshopper</a> - extremely popular graphical node-based algorithm editor tightly integrated with Rhino’s 3D modeling tools. Highly recommended for digital morphogenesis work. Was a third-party plugin for many years, but is now a part of Rhino 6+.</li>
              <li><a href="https://www.food4rhino.com/app/lunchbox" target="_blank">Lunchbox</a> - very powerful collection of utilities for generative geometry, math, data manipulation, and even machine learning.</li>
              <li><a href="https://www.food4rhino.com/app/kangaroo-physics" target="_blank">Kangaroo</a> - live physics engine for interactive simulation, form-finding, optimization and constraint solving.</li>
            </ul>
          </p>
        </details>
      </td>
    </tr>
    <tr>
      <td><a href="http://structuresynth.sourceforge.net/" target="_blank">Structure Synth</a></td>
      <td>Application for generating surprising and complex fractal 3D structures using a design grammar.</td>
      <td>Free</td>
    </tr>
    <tr>
      <td><a href="https://www.derivative.ca/" target="_blank">TouchDesigner</a></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><a href="https://unity.com/" target="_blank">Unity</a></td>
      <td></td>
      <td>Free for hobbyists</td>
    </tr>
    <tr>
      <td><a href="https://www.unrealengine.com/en-US/)" target="_blank">Unreal</a></td>
      <td></td>
      <td>Free with <a href="https://www.unrealengine.com/en-US/faq" target="_blank">royalty on commercial products</a></td>
    </tr>
  </tbody>
</table>

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
* Viscous fingering, a.k.a. Saffman–Taylor instability
* Percolation theory
* Flow field (math or code concept?)
* Soap experiments (see Frei Otto)