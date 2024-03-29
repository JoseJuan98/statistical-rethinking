# Chapter 1 Notes - The Golem of Prague

## Summary of ideas

* Analogy of scientific models with the Golem of Prague
* Statistics should be seen as a set of design principles and constraints that produces a
great diversity of specialized applications, like engineering.
* Statistical inference's goal is not to test null hypothesis, because:
    * Models are not hypothesis
    * Data measurements matters
* "Science advances by falsifying hypotheses", Karl Popper. It's common
among scientists but not among philosophers of science,but it doesn't work,
but it helps to open the eyes to know how statistics works.
* Statistical models expresses associations among variables, so to make one it's needed to
derive the expected frequency distribution of some quantity - "statistics" - from the casual model.
* Models purposes: designing inquiry, extraction information from data, and making predictions.
    * Bayesian data analysis
    * Model comparison
    * Multilevel analysis
    * Grpachical causal models



## Details
### Golem of Prague

Decision tree, or flowchart, for selecting an appropriate statistical procedure.

![Decision Tree St Models](img/1_PragueGolem.png)


No statistical tool does anything on its own to address the basic problem
of inferring causes from evidence. Statistical golems do not understand cause and effect.
They only understand association. Without our guidance and skepticism, pre-manufactured
golems may do nothing useful at all. Worse, they might wreck Prague.

Rather than idealized angels of reason, scientific models are powerful clay
robots without intent of their own. Sometimes their unyielding logic reveals
implications previously hidden to their designers. These implications can
be priceless discoveries, or they may produce silly and dangerous behavior.

It's a triumph of statistical science that there are now so many diverse models,
each useful in a particular context. Viewed this way, statistics is neither mathematics
nor a science, but rather a branch of engineering. And like engineering, a common set of
design principles and constraints produces a great diversity of specialized applications.


## Rethinking statistics

What researchers need is some unified theory of model engineering, a set of principles for
designing, building, and refining special-purpose statistical procedures. Every major branch
of statistical philosophy possesses such a unified theory. But the theory is never taught in
introductory—and often not even in advanced—courses. So there are benefits in **rethinking
statistical inference as a set of strategies**, instead of a set of pre-made tools.

If you don’t understand how the model processes information, then you can’t interpret the
model’s output. This requires knowing the statistical model in greater detail than is
customary, and it requires doing the computations the hard way, at least until you are
 wise enough to use the push-button solutions.

Understanding any individual model is not enough,
in these cases. Instead, we need some statistical epistemology, an appreciation of how
statistical models relate to hypotheses and the natural mechanisms of interest.

Most of the people think that statistical inference's goal is to test null hypothesis, so 
"statistical procedures may falsify hypothesis to be good statistical scientist". But this
is false because:
1. Hypothesis are not models. Many hypothesis correspond to one model and many models can
correspond to a single hypothesis.
   
2. Measurements matters. When data falsify a model, sometimes this model won't be a right
model.
   
Falsification to prove that it won't work is not good science, but it helps to open the eyes
to know how statistics works.

Deductive falsification never works, the scientific method cannot
be reduced to a statistical procedure, and so our statistical methods should not pretend. Statistical 
evidence is part of the hot mess that is science, with all of its combat and egotism and
mutual coercion. If you believe that science does often work, then learning that it
doesn’t work via falsification shouldn’t change your mind. But it might help you do better
science, because it will open your eyes to many legitimately useful functions of statistical
golems.


### Hypothesis are not models

![1_2_Hypothesis](/img/1_2_Hypothesis.png)

Relations among hypotheses (left), detailed process models
(middle), and statistical models (right), illustrated by the example of “neutral” models of evolution. 
Hypotheses (H) are typically vague, and so correspond to more than one process model (P). Statistical
evaluations of hypotheses rarely address process models directly. Instead, they rely upon
statistical models (M), all of which reflect only some aspects of the process
models. As a result, relations are multiple in both directions: Hypotheses
do not imply unique models, and models do not imply unique hypotheses.
This fact greatly complicates statistical inference.

Unfortunately, statistical models do not embody specific causal relationships. A
statistical model expresses associations among variables. As a result, many different process
models may be consistent with any single statistical mode

How do we get a statistical model from a causal model? One way is to derive the expected frequency 
distribution of some quantity—a “statistic”—from the causal model.

The classical approach is to take the “neutral” model as a null hypothesis. If the data are not 
sufficiently similar to the expectation under the null, then we say that we “reject” the null hypothesis.
Suppose we follow the history of this subject and take P 0A as our null hypothesis. This implies
data corresponding to M II . But since the same statistical model corresponds to a selection
model P 1B , it’s not at all clear what we are to make of either rejecting or accepting the null.
The null model is not unique to any process model nor hypothesis. If we reject the null,
we can’t really conclude that selection matters, because there are other neutral models that
predict different distributions. And if we fail to reject the null, we can’t really conclude
that evolution is neutral, because some selection models expect the same frequency distribution.

Statistical models can be confused in other ways as well, such as the confusion caused by
unobserved variables and sampling bias. Process models allow us to design statistical models
with these problems in mind. The statistical model alone is not enough

### Measurement matters
Most of the problems scientists confront are not logically discrete. Instead, we most often face two 
simultaneous problems:
* First, observations are prone to error, especially at the boundaries of scientific knowledge.
* Second, most hypotheses are quantitative, concerning degrees of existence, rather than discrete, 
  concerning total presence or absence. Let’s briefly consider each of these problems.
* Third, falsification can be consensual, not logical. In light of the real problems of measurement
  error and the continuous nature of natural phenomena, scientific communities argue towards 
  consensus about the meaning of evidence. These arguments can be messy. After the fact, some
  textbooks misrepresent the history so it appears like logical falsification.
  
## Tools for Model Engineering
### Bayesian Data Analysis
Bayesian data analysis takes a question in the form of a model
and uses logic to produce an answer in the form of probability distributions.

"We just use randomness to describe our uncertainty in the face of incomplete knowledge."

Note that the preceding description doesn’t invoke anyone’s “beliefs” or subjective opinions. 
Bayesian data analysis is just a logical procedure for processing information.

Not only is there “Bayesian” and “frequentist” probability, e.g. the “logical” Cox 
(or Laplace-Jeffreys-Cox-Jaynes) interpretation.

#### Model comaprison and prediction

Bayesian data analysis provides a way for models
to learn from data. But when there is more than one plausible model—and in most mature
fields there should be—how should we choose among them? One answer is to prefer models
that make good predictions. This answer creates a lot of new questions, since knowing which
model will make the best predictions seems to require knowing the future.
**Cross validation** and **information criteria**, these tools aim to let us compare models
based upon expected predictive accuracy.

Often complex models make worse predictions than simpler models. This is called 
the Overfitting paradox: "fitting is easy, prediction is hard". Future data won't be like
past data. Cross validation and information critieria can measure overfitting.

#### Multilevel models

They are models which each model is feeding into next. They help to solve the overfitting 
problem with **Partial Pooling**. They are good in cases like models for missing data 
(imputation), measurement error, factor analysis, some time series models, types of spatial 
and network regression, and phylogenetic regressions.

Multilevel models should be the default model to use, because even when well-controlled variables
interact with unmeasured aspects of the individuals, groups, or populations studied. Multilevel models
attempt to quantify the extent of this variation, as well as identify which units in the data responded
in which ways.

These benefits don’t come for free, however. Fitting and interpreting multilevel models can be 
considerably harder than fitting and interpreting a traditional regression model.

#### Graphical Causal Models

Statistical models are never sufficient for inferring cause because it doesn't make a distinction.
Facts outside the data are needed to decide which explanation is correct.

Another paradox of Bayesian Data Analysis: "Models causally incorrect can make better predictions
than those that are causally correct". Also known as the **Identification problem**. So,
successful prediction doesn't require correct causal identification. predictions can
improve when we use a model that is causally misleading.

Causal inference requires a causal model that is separate from the statistical
model. The data are not enough. We need a causal model used for design statistical models for causal 
identification. But even when you don’t have a complete causal model, but
only a heuristic one indicating which variables causally influence others, you can still make
use of these logical tools, such ase a graphical causal model to represent a causal hypothesis.

The simplest graphical causal model is a directed acyclic graph, usually called a DAG. 
DAGs are heuristic—they are not detailed statistical models. But they allow us to deduce 
which statistical models can provide valid causal inferences.

The approach which dominates in many parts of biology and the social sciences is instead
causal salad.36 Causal salad means tossing various “control” variables into a statistical model,
observing changes in estimates, and then telling a story about causation. Causal salad seems founded
on the notion that only omitted variables can mislead us about causation. But included variables can
just as easily confound us. When tossing a causal salad, a model that makes good predictions may still
mislead about causation. If we use the model to plan an intervention, it will get everything wrong.

