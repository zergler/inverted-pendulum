# inverted-pendulum
A survey of reinforcement learning solutions to the inverted pendulum problem.

# Introduction
The inverted pendulum problem can be defined concisely as creating a system
that autonomously balances a rotating pendulum attached to a cart on a rail
using actuators to move the cart along the rail, and sensors to reveal the
state of the cart and pendulum. Given a specific inverted pendulum system,
solving the problem amounts to choosing which sensors to use, optionally
formulating a deterministic or stochastic model that approximates the physics
involved, and most importantly figuring out a control strategy that works.
It is a classic problem in control theory and dynamics and can serve as a good
testing ground for the development of real-time control algorithms. A good
argument for the motivation of understanding the problem can be seen by noting
its prevalence in nature and the man made world. For example, every person when
upright needs to constantly make adjustments to prevent from falling over, and
so all of us repeatedly solve a much more difficult version of this problem
when sitting or moving about.

# Problem Formulation
A pendulum of length **l** with a mass **m** on one end and attached to a cart
of mass **M** with a hinge, is able to rotate by the effect of the application of
some force **F** on the cart.


![Alt text](/img/pendulum.png?raw=true "Schematic of the problem setup. Graphic by Krishnavedala, Wikimedia commons (CC0 1.0).")

By assumption, the friction of the cart on the ground as well as the friction
of the pendulum on the cart are ignored.  The cart is limited to motion in the
horizontal x-axis, while the pendulum is able to rotate along the x, y plane
freely, making an angle of **θ** with the y-axis. It is also assumed that the
force vector **F** has no component in the y direction. A controller attempts
to balance the pendulum by applying a finite force to the cart, allowing it to
move left or right with some acceleration. After some amount of time **∆T** has
passed, the controller fails if either the angle of the pendulum deviates by
more than **±∆θ** or the position of the cart reaches the bounds **±L**. The
problem can now be stated explicitly: develop a controller that balances the
pendulum under these constraints.

# References
The following list contains background research material.

[1] Stimac, Andrew K. Standup and stabilization of the inverted pendulum. Diss.
Massachusetts Institute of Technology, 1999.

[2] Russell, Stuart, and Peter Norvig. "Artificial intelligence: a modern
approach." (1995).

[3] Sutton, Richard S., and Andrew G. Barto. Reinforcement learning: An
introduction. Vol. 1. No. 1. Cambridge: MIT press, 1998.

[4] Melo, Francisco S., Sean P. Meyn, and M. Isabel Ribeiro. "An analysis of
reinforcement learning with function approxi- mation." Proceedings of the 25th
international conference on Machine learning. ACM, 2008.

[5] Kober, J. & Peters, J. (2012). Reinforcement learning in robotics: A
survey. In Reinforcement Learning, Vol. 12 of Adaptation, Learning, and
Optimization, pp. 579-610. Springer Berlin Heidelberg.

[6] Anderson, Charles W. "Learning to control an inverted pendulum using neural
networks." Control Systems Magazine, IEEE 9.3 (1989): 31-37.

[7] Watkins, Christopher JCH, and Peter Dayan. "Q-learning." Machine learning
8.3-4 (1992): 279-292.

[8] Krizhevsky, Alex, Ilya Sutskever, and Geoffrey E. Hinton. "Imagenet
classification with deep convolutional neural net-
works." Advances in neural information processing systems. 2012.

[9] Mnih, Volodymyr, et al. "Playing atari with deep reinforcement learning."
arXiv preprint arXiv:1312.5602 (2013).

