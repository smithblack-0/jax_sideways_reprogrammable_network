# Goals

The overall architecture goals stand as follows

* Develop a model with relatively straightforward plug-n-play capacity between model instances
* Develop a model that can easily be extended into performing external actions and fetching results
* Develop a model that is still trainable by gradient descent, at least the majority of the time.
* Develop a model that does not waste excess computation time, or execute processes that are not needed
* Develop a model that can be configured to process different tasks, such as image generation or text processing,
  by adjusting the layers or underlying functions.
* Develop a model that is faster to learn and uses less parameters by reusing existing
  features while training.

# Design Decisions

## Interface:
  * The model will be designed to be recurrent.
  * The model will accept an input state, and any recurrent state it has created 
    or needs
  * The model will need to produce an output answer, and recurrent state 


## Internal Architecture: Overview
  * The model will posses an ACT architecture capable of pondering a situation until
    it feels ready to return.
  * The model will possess a large number of internal layers. These layers are
    not sequential, but may be accessed at random from any processing step.
  * The model will possess a controller. This controller will be responsible
    for deciding what to do next.

## Processing Plug-n-play layers

* For ease of simplicity, there will 
## ACT loop

* An act loop will exist
* Any number of ACT features may be accumulated at once
* Each iteration, the act mechanism must be presented with a halting 
  probabilities tensor.

## ACT loop

  * The model will have an intermediate state it can use when processing.
  * The model will have any number of internal layers. These layers can be called
    to process features when the model deems it wise.
  * A controller exists. It determines what layers are called, and in what order.
  * 



* Develop a model that can be configured to process something sequentially.
* This model should be easily extendable with new, possibly novel layers. 
* This model should all