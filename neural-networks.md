
---

## Neural-Networks

**What is a neuron? **

Neurons \(also called neurones or nerve cells\) are the fundamental units of the brain and nervous system, the cells responsible for receiving sensory input from external world, for sending motor commands to our muscles, and for transforming and relaying the electrical signals at every step in between.

**What does a neuron look like?**

A useful analogy is to think of a neuron as a tree. A neuron has three main parts: **dendrites**, an **axon** and a **cell body or soma**, which can be represented as the branches, roots and trunk of a tree, respectively. A dendrite \(tree branch\) is where a neuron receives input from other cells. Dendrite branch as they move towards their tips, just like tree branches do, and they even have leaf-like structures on them called spines.

The **axon \(tree roots\)** is the output structure of the neuron; when a neuron wants to talk to another neuron, it sends an electrical message called an action potential through the entire axon. The **soma \(tree trunk\)** is where the _**nucleus lies**_, where the neuron's DNA is housed, and where proteins are made to be transported throughout the **axon and dendrites**.

![](/assets/import.png)**Axon -** The long, thin structure in which action potentials are generated; the transmitting part of the neuron. After initiation, action potentials travel down anons to cause release of neurotransmitter.

**Dendrite - **The receiving part of the neuron. Dendrites receive synaptic inputs from axons, with the sum total of dendritic inputs determining whether the neuron will fire an action potential.

**Spine - **The small protrusions found on dendrites that are, for many synapses, the postsynaptic contact site.

**Action potential** - Brief electrical event typically generated in the axon that signals the neuron as 'active'. An action potential travels the length of the axon and causes release of neurotransmitter into the synapse. The action potential and consequent transmitter release allow the neuron to communicate with other neurons.

### Types of neurons

Neurons are the cells that make up the brain and the nervous system. They are fundamental units that send and receive signals which allow us to move our muscles, feel the external world, think form memoriesand much more.

For the spinal cord though, we can say that there are three types of neurons: sensory, motor, and interneurons.

**Sensory neurons** - are the nerve cells that are activated by sensory input from enviroment;  for example, when you a hot surface with your fingertips, the sensory neurons will be the ones firing and sending off signals to the rest of the nervous system about the information they have received.  The inputs that activate sensory neurons can be physical or chemical, corresponding to all five of our senses.

**Motor neurons** - motor neurons of the spinal cord are part of the central nervous system \(CNS\) and connect to muscles, glands and organs throughout the body. These neurons transmit impulses from the spinal cord to skeletal and smooth muscles, and so directly control all of our muscle movements. _There are in fact two type of motor neurons: those that travel between the brain and spinal cord are called upper motor neurons. _

**Interneurons** - are the ones in between -- they connect spinal motor and sensory neurons. As well as transferring signals between sensory and motor neurons, interneurons can also communicate with each, forming circuits of various complexity. They are multipolar, just like motor neurons.

## **The Simple Perceptron **

**Artificial Neural Network**

* Information processing architecture  loosely modeled on the brain. 
* Consist of large number of interconnected processing units \(neurons\)
* Work in parallel to accomplish a global task 
* Generally used to model relations between inputs and outputs or find patterns in data.
* 3 types of layers \(Input layer, Hidden layer, Output layer\)

![](/assets/Screen Shot 2018-04-27 at 10.49.54 AM.png)

![](/assets/Screen Shot 2018-04-27 at 10.50.43 AM.png)

**Network Structure **

1. Feed-Forward Network
2. Recurrent Network

**Learning Paradigms **

* Supervised Learning: 
  * Given training data consist of pairs of input/outputs, find a function which correctly matches them.
* Unsupervised Learning:

  * Given a data set, the network find patterns and categorizes into data groups.

**Reinforcement Learning:**

* No data given. Agent interacts with the enviroment calculating cost of actions. 

#### **Simple Perceptron**

* The perceptron is a single layer feed-forward neural network. 

#### Linearly Separable

* The bias is poportional to the offset of the plane from the origin.
* The weights determine the slope of the line.
* The weight vector is perpendicular to the plane.

### Perceptron Learning Algorithm

* We want to train the perceptron to classify inputs correctly
* Accomplished by adjusting the connecting weights and the bias 
* Can only properly handle linearly separable sets

### Perceptron Learning Algorithm

* We have a "training set" which is a set of input vectors used to train the perceptron

* During training both Wi and 0 \(bias\) are modified for convenience, let W0 = 0 \(bias\) are modified for convenience, let W0 = 0 and x0 = 1.

* Let n the learning rate, be a small positive number \(small steps lessen the possibility of destroying correct classification\).

* Initialize Wi to some values.

* Select random sample from training set as input.

* If classification is correct,do nothing.

* If classification is incorrect,modify the weight vector w using Wi = Wi + nd\(n\) xi\(n\)

Repeat this procedure until the entire training set is classified correclty.

### Perceptron Convergence Theorem

* The theorem states that for any data set which is linearly separable, the perceptron learning rule is guaranteed to find a solution in a finite number of iterations. 
* Idea behind the proof: Find upper & lower bounds n the length of the weight vector to show finite number of iterations. 

Perceptron has just 2 layers of nodes \(input node and output node\). Often called a single-layer network on account of having 1 layerof links, between input and output.

**Fully connected? **

Note to make an input node irrelevant to the output, set its weight to zero. If w1 = 0 here, then Summed input is the same no matter what is in the 1st dimension of the input.

Weights may also become negative \(higher positive input tends to lead to not fire\).

Some inputs may be positive, some negative \(cancel each other out\).

**The Brain**

A similarkindof thing happens in neurons in the brain \(if excitation greater than inhibition, send a spike of electrical activity on down the output axon\), though researchers generally aren't concerned if there are differences between their models and natural ones.

* Big breakthrough was proof that you could wire up certain class of artificial nets to form any general-purpose computer.
* Other breakthrough was discovery of powerful learning methods, by which nets could learn to represent initially unknown I-O relationships \(see previous\). 

---

_If every class in the ImageNet training has an equal number of examples_

_\(so 1300000/1000=1300\) and the test set is similarly balanced, then what is the expected top-1 error rate of a system that guesses the class of each image uniformly at random? What is the expected top-5 error rate? The top-k error rate is the proportion of test set examples whose correct label isnotamong the top-k predictions of the network._

_**0.9987, 0.995**_

There are10001000classes, so if we just choose randomly then the probability of choosing correctly is 1/1000​=0.001. The error rate is defined as E\[\# examples labelled incorrectly\] /\#examples = ∑examples P\(example guessed incorrectly\)/\# examples= \(1−0.001\)×\# examples\# /examples=0.999. In other words, it is the probability of guessing any single example incorrectly. Using this naive method we would expect to mislabel 99.9 of the test set!

If we randomly choose55classes instead, the probability of correctly guessing the class of an example is 5/1000​, so the expected error rate is 0.995. By comparison, a learning system can get much larger improvements.

#### Modularity and the brain

* Different bits of the cortex do different things.

  * Local damage to the brain has specific effects.
  * Specific tasks increase the blood flow to specific regeions. 

* But cortex looks pretty much the same all over.

  * Early brain damage makes functions relocate. 

* Cortex is made of general purpose stuff that has the ability to turn into special purpose hardware in reponse to esperience.

  * This gives a rapid parallel computation plus flexibility.

  * Conventional computers get flexibility by having stored sequential programs, but this require very fast central processors to perform long sequential computations.

**1-** _We often don't know how much data we will need in order for a learning system to generalize well from training data to test data on a given task._

_True or false: when choosing how much data to give to a learning system in order to make it generalize well, we need to make sure that we don't give it too much data. _**False**

**2-**_ Data can change over time, in particular we might observe different input/output relationships. In order to account for this we can adapt our learning system to the new data by, for example, training on new examples._

_If the relationship between inputs and outputs for old examples has not changed, how can we prevent a neural network from forgetting about the old data?_

* Train on a mix of old and new data. 
* Prevent the system from changing the weights too much.
* Ignore the issue and hope that everything will be OK.

**3- **_Which of the following are good reasons for why are interested in unsupervised learning?_

* It allows academic researchers to publish more papers.

* It can be used to learn features that may help with supervised tasks.

* It allows us to learn from vast amounts of unlabelled data.

**4- **Which of the following tasks are neural networks good at?

* Recognizing fragments of words in a pre-processed sound wave. 
* Recognizing badly written characters. 
* Storing lists of names and birth dates.

**5-** Which number is biggest?

The number of synapes in a human brain.

**6-** Which of the following facts provides support for the  theory that the local neural circuits in most parts of the cortex all use the same general purpose learning algorithm?

* If part of the cortex is removed early life, the function that would have served often gets relocated to another part of cortex.
* The fine-scale anatomy of the cortex looks pretty much the same all over.

---

## WEEK 2

#### Feed-forward neural networks

* These are the commonest type of neural networks in practical applications. 
  * The first layer is the input and the last layer is the output. 
  * If there is more than one hidden layer, we call them "deep" neural networks
* They compute a series of transformations that change the similarities between cases. 
  * The activities of the neurons in each layer are a non-linear function of the activities in the layer below.

#### Recurrent networks

* These have directed cycles in their connection graph.
  * That means you can sometimes get back to where you started by following the arrows.
* They can have complicated dynamics and this can make them very difficult to train.
  * There is a lot of interest at present in finding efficient ways of training recurrent nets.
* They are more biologically realistic.

#### Recurrent neural networks for modeling sequences

* Recurrent neural networks are a very natural way to model sequential data:
  * They are equivalent to very deep nets with one hidden layer per time slice. 
  * Except that they use the same weights ate every time slice and they get input at every time slice. 
* They have the ability to remember information in their hidden state for a long time.
  * But its very hard to train them to use this potential.

#### An example of hat recurrent neural nets can now do

Ilya Sutskever \(2011\) trained a special type of recurrent networks to predict the next character in a sequence.

After training for a long time  on a string of half a billion characters from English Wikepedia, he got it to generate new text.

* It generates by predicting the probability distribution for the next character and then sampling a character from his distribution.
* The next slide show an example of the kind of text it generates. Notice how much it knows.

#### Symmetrically connected networks

These are like recurrent networks, but the connections between units are symmetrical \(they have the same weight in both  directions\).

* John Hopfield \(and others\) realized that symmetric networks are much easier to analyze than recurrent networks. 
* They are also more restricted in what they can do, because they obey an energy function. 
  * For example, they cannot model cycles.
* Symmetrically connected nets without hidden units are called "Hopfield nets".

#### Symmetrically connected networks with hidden units

* These are called "Boltzmann machines"
  * They are much more powerful models than Hopfield nets.
  * They are less powerful than recurrent neural networks.
  * They have a beautifully simple learning algorithm.

## The first generation of neural networks

The standard paradigm for statistical pattern recognition

1. Convert the raw input vector into a vector of feature activations. 
   1. Use hand-written programs based on common-sense to define the features.
2. Learn how to weight each of the feature activations to get a single scalar quantity.
3. If this quantity is above some threshold, decide that the input vector is a positive example of the target class.

### The history of perceptrons

They were popularised by Frank Rosenblatt in the early 1960's.

* They appeared to have a very powerful learning algorithm. 
* Lots of grand claims were made for what they could learn to do.

In 1969, Misky and Papert published a book called "Perceptrons" that analysed what they could do and showed their limitations.

* Many people thought these limitations applied to all neural network models.

The perceptron learning procedure is still widely used today for tasks with enormous feature vectors that contain many millions of features.

#### Binary threshold neurons \(decision units\)

McCullouch-Pitts\(1943\)

* First compute a weighted sum of the inputs from other neurons \(plus a bias\)
* Then output a 1 if the weighted sum exceeds zero.

#### How to learn biases using the same rule as we use for learning weights

* A threshold is equivalent to having a negative bias. 
* We can avoid having to figure out a separate learning rule for the bias by using a trick:
  * A bias is exactly equivalent to a weight on a n extra input line that weight on an extra input line that always has an activity of 1. 
  * We can now learn a bias as if it were a weight.

##### The perceptron convergence procedure: Training binary output neurons as classifiers

* Add an extra component with value 1 to each input vector.The "bias" weight on this component is minus the threshold: Now we can forget the threshold.
* Pick training classes using any policy that ensures that every training case will keep getting picked.
  * If the output unit is correct, leave its weights alone.
  * If the output unit incorrectly outputs a zero, add the input vector to the weight vector.
  * If the output unit incorrectly outputs a 1, subtract the input from the weight vector.
* This is guaranteed to find a set of weights that gets the right answer for all the training cases if any such set exists.

#### A geometrical view of perceptrons

**Weight-space**

This space has one dimension per weight.

A point in the space represents a particular setting of all the weights.

Assuming that we have eliminated the threshold, each training case can be represented as hyperplane through the origin.

* The weights must lie on one side of this hyper-plane to get the answer correct.
* Each case defines a plane \(shown as a black line\)

  * The plane goes through the origin and is perpendicular to the input vector.
  * On one side of the plane the output is wrong because the scalar product of the weight vector with the input vector ha the wrong sign.

* Each training case defines a plane \(shown as a black line\)

  * The plane goes through the origin and is perpendicular to the input vector.
  * On one side of the plane the output is wrong because the scalar product of the weight vector with the input vector has the wrong sign. 

#### The cone of feasible solutions

* To get all training cases right we need to find a point on the right side of all the planes.
  * There may not be any such point!
* If there are any weight vectors that get the right answer for all cases, they lie in a hyper-cone with its apex at the origin.
  * So the average of two good weight vectors is a good weight vector.
    * The problem is convex.

**Why the learning procedure works**

Consider the squared distance d^2a +d^b between any feasible weight vector and the current weight vector.

* Hopeful claim: Every time the perceptron makes a mistake, the learning algorithm moves the current weight vector closer to all feasible weight vectors.

So consider "generously feasible" weight vectors that lie within the feasible region by a margin at least as great as the length of the input vector that defines each constraint plane.

* Every time perceptron makes a mistake, the squared distance to all of these generously feasible weight vectors is always decreased by at  least the squared length of the update vector.

**Informal sketch of proof of convergence** 

* Each time the perceptron makes a mistake, the current weight vector moves to decrease its squared distance from every weight vector in the "generously feasible" region.
* The squared distance decreases by at least the squared length of the input vector.
* So after a finite number of mistakes, the weight vector must lie in the feasible region if this region exists.

**The limitations of Perceptrons **

If you are allowed to choose the the features by hand and if you use enough features, you can do almost anything. 

* For binary input vectors, we can have a separate feature unit for each of the exponentially many binary vectors and so we can make any possible discrimination on binary input vectors.
  * This type of table look-up won't generalize.
* But once the hand-coded features have been determined, there are very strong limitations on what a perceptron can learn.





