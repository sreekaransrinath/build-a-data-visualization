# build-a-data-visualization
MLH Local Hack Day: Build 2021 Day 3 Task: Build a Data Visualization

## Task Statement
Data science is one of the fastest growing fields in tech. There are so many different ways to visualize data. It can be as simple as a graph or as complex as a piece of art. Show off your visualization on the Day 3 Devpost when you’re finished.

# Submission

## Visualizing the generation of chaos from a deterministic system
For the Day 2 Challenge "Create a Random Number Generator", I used the logistic map to generate a pseudo-random number [here](https://github.com/sreekaransrinath/create-a-random-number-generator).

Today's challenge is a perfect follow up to that. Let's visualize how the logistic map starts off in a perfectly orderly fashion, before descending into chaos.

## But first, what _is_ a logistic map?

## An Introduction
What's the connection between a dripping faucets, the Mandelbrot set, a population of rabbits, thermal convection in a fluid, and the firing of neurons in your brain?
It's this one simple equation -
![Logistic Map Equation](https://mathworld.wolfram.com/images/equations/LogisticMap/NumberedEquation2.gif)

(known as the discrete logistic equation or logistic map).

The logistic map is a one dimensional map that, for certain parameter values, can give rise to chaos; this lets us generate pseudo-random numbers from a deterministic process.

This equation defines the rules, or dynamics, of our deterministic system: x represents the population at any given time t, and r represents the growth rate. In other words, the population level at any given time is a function of the growth rate parameter and the previous time step’s population level. If the growth rate is set too low, the population will die out and go extinct. Higher growth rates might settle toward a stable value or fluctuate across a series of population booms and busts.
![](https://i2.wp.com/geoffboeing.com/wp-content/uploads/2015/03/logistic-model-line.png?resize=624%2C359&ssl=1)

As simple as this equation is, it produces chaos at certain growth rate parameters.

When we adjust the growth rate parameter beyond 3.5, we see the onset of chaos. A chaotic system has a strange attractor, around which the system oscillates forever, never repeating itself or settling into a steady state of behavior. It never hits the same point twice and its structure has a fractal form, meaning the same patterns exist at every scale no matter how much you zoom into it.

![](https://i2.wp.com/geoffboeing.com/wp-content/uploads/2015/03/logistic-bifurcation-full1.png?w=613&ssl=1)

Beyond a growth rate of 3.6, however, the bifurcations ramp up until the system is capable of eventually landing on any population value. This is known as the period-doubling path to chaos. As you adjust the growth rate parameter upwards,  the logistic map will oscillate between two then four then eight then 16 then 32 (and on and on) population values. These are periods, just like the period of a pendulum.

By the time we reach growth rate 3.9, it has bifurcated so many times that the system now jumps, seemingly randomly, between all population values. I only say seemingly randomly because it is definitely not random. Rather, this model follows very simple deterministic rules yet produces apparent randomness. This is chaos: deterministic and aperiodic.

![](https://i1.wp.com/geoffboeing.com/wp-content/uploads/2015/03/logistic-bifurcation-narrow1.png?w=616&ssl=1)


Borrowing content from Data Scientist Geoff Boeing and Educator Derek Muller,

Chaotic systems are also characterized by their sensitive dependence on initial conditions. They don’t have a basin of attraction that collects nearby points over time into a fixed-point or limit cycle attractor. Rather, with a strange attractor, close points diverge over time.

This makes real-world modeling and prediction difficult, because you must measure the parameters and system state with infinite precision. Otherwise, tiny errors in measurement or rounding are compounded over time until the system is thrown drastically off. It was through one such rounding error that Lorenz first discovered chaos. Recall his words at the beginning of this piece: “the present determines the future, but the approximate present does not approximately determine the future.”

As an example of this, let’s run the logistic model with two very similar initial population values:
![](https://i2.wp.com/geoffboeing.com/wp-content/uploads/2015/03/logistic-sens-dep-init-cond.png?w=606&ssl=1)

Both have the same growth rate parameter, 3.9. The blue line represents an initial population value of 0.5. The red line represents an initial population of 0.50001. These two initial conditions are extremely similar to one another. Accordingly their results look essentially identical for the first 30 generations. After that, however, the minuscule difference in initial conditions starts to compound. By the 40th generation the two lines show little in common.

If our knowledge of these two systems started at generation 50, we would have no way of guessing that they were almost identical in the beginning. With chaos, history is lost to time and prediction of the future is only as accurate as your measurements. In real-world chaotic systems, measurements are never infinitely precise, so errors always compound, and the future becomes entirely unknowable given long enough time horizons.

This is famously known as the butterfly effect: a butterfly flaps its wings in China and sets off a tornado in Texas. Small events compound and irreversibly alter the future of the universe. In the line chart above, a tiny fluctuation of 0.00001 makes an enormous difference in the behavior and state of the system 50 generations later.

The Implications of Chaos
Real-world chaotic and fractal systems include leaky faucets, ferns, heart rates, and random number generators. Many scholars have studied the implications of chaos theory for the social sciences, cities, and urban planning. Chaos fundamentally indicates that there are limits to knowledge and prediction. Some futures may be unknowable with any precision. Deterministic systems can produce wildly fluctuating and non-repeating behavior. Interventions into a system may have unpredictable outcomes even if they initially change things only slightly, as these effects compound over time.

During the 1990s, complexity theory grew out of chaos theory and largely supplanted it as an analytic frame for social systems. Complexity draws on similar principles but in the end is a very different beast. Instead of looking at simple, closed, deterministic systems, complexity examines large open systems made of many interacting parts. Unlike chaotic systems, complex systems retain some trace of their initial conditions and previous states, through path dependence. They are unpredictable, but in a different way than chaos: complex systems have the ability to surprise through novelty and emergence.