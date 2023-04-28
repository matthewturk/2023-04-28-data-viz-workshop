<!-- .slide: class="titleslide" -->

# Data Storytelling and Mental Models of Data in the Natural Sciences

## Matthew Turk

<p data-markdown=true>School of Information Sciences<br/>
University of Illinois at Urbana-Champaign<br/>
<tt>mjturk@illinois.edu</tt><br/>
<tt>matthewturk.github.io</tt></p>

---

## Thank you

Before I begin, I want to say thank you for inviting me to give this talk today.

I'm really glad I get to meet all of you, and share with you some ideas about
visualization.

<div class="fragment">(to be honest I'm more than a little intimidated, so bear with me)</div>

---

## Who Am I

<ul>
<li class="fragment">Computational <b>astrophysicist</b> by training</li>
<li class="fragment">Developed simulation platforms and analysis <b>tools</b> for astrophysics</li>
<li class="fragment">Worked in interdisciplinary applications, study <b>communities</b> of practice in open source scientific software</li>
<li class="fragment">Tenure-track at the School of Information Sciences, developing and implementing a <b>grammar</b> of volumetric analysis
</ul>

---

## Credits: Local

<div class="multiCol">
<div class="col" data-markdown=true>

![Samantha Walkow](https://raw.githubusercontent.com/data-exp-lab/data-exp-lab.github.io/4ff6549d71c67b62b958fa6d8ff66c3dd2a13356/assets/img/people/swalkow.jpg) <!-- .element: class="headshot" -->

Samantha Walkow <!-- .element: class="headshot-caption" -->

</div>

<div class="col" data-markdown=true>

![Kate McDowell](images/KateMcDowell.jpg) <!-- .element: class="headshot" -->

Prof. Kate McDowell <!-- .element: class="headshot-caption" -->

</div>

<div class="col" data-markdown=true>

![Karen Wickett](images/KarenWickett.jpg) <!-- .element: class="headshot" -->

Prof. Karen Wickett <!-- .element: class="headshot-caption" -->

</div>
</div>

<div class="multiCol">
<div class="col" data-markdown=true>

![Jill Naiman](images/JillNaiman.png) <!-- .element: class="headshot" -->

Dr. Jill Naiman <!-- .element: class="headshot-caption" -->

</div>

<div class="col" data-markdown=true>

![Chris Havlin](https://raw.githubusercontent.com/data-exp-lab/data-exp-lab.github.io/4ff6549d71c67b62b958fa6d8ff66c3dd2a13356/assets/img/people/chavlin.jpg) <!-- .element: class="headshot" -->

Chris Havlin <!-- .element: class="headshot-caption" -->

</div>
</div>

---

## Let's Center Ourselves

Before we get too far, I want to set the stage for how *I* got here.

<p class="fragment">(I mean, we're all the protagonists of our own stories, right?)</p>

---

## Cartoon History of the Universe

<div class="multiCol">
<div class="col">
<div class="fig-container" data-style="height: 600px;" data-file="/2019-12-09-qmc-hamm-research-overview/figures/collapse_heating.html" data-markdown=true>
</div>
</div>
<div class="col" data-markdown=true>
<p class="fragment" data-fragment-index="0">After recombination, the universe was in a nearly-but-not-totally homogeneous state, seeded with instabilities and with a few residual electrons.</p>
<div class="fragment" data-fragment-index="1">
<p>Early-on, dark matter clumps collected and formed "halos," drawing in baryonic material.</p>
<p>This process converted potential energy into thermal energy, heating the baryonic matter, which shed the thermal energy through radiative processes.</p>
</div>
<p class="fragment" data-fragment-index="2">Eventually, this cloud becomes fully-molecular through the three-body interaction and forms an accretion disk.</p>
</div>
</div>

---

## The Storytelling Triangle

<div class="multiCol">
<div class="col">

<p class="fragment" data-fragment-index="0">Borrowing from Kate McDowell's framing, we can think of three components in our triangle.</p>

<ul>
<li class="fragment" data-fragment-index="1">The Storyteller</li>
<li class="fragment" data-fragment-index="2">The Tale</li>
<li class="fragment" data-fragment-index="3">The Audience</li>
</ul>

</div>
<div class="col">
<div class="fig-container" data-file="figures/storytelling.html" data-preload data-style="width: 700px;">
</div>

---

## The Storytelling Triangle

Let's think about three potential categories of visualization: <!-- .element: class="fragment" data-fragment-index="1" -->

<div class="multiCol">
    <div class="col">
        <ul>
            <li class="fragment" data-fragment-index="2">Visualizations we make for ourselves</li>
            <li class="fragment" data-fragment-index="3">Visualizations we make for our peers</li>
            <li class="fragment" data-fragment-index="4">Visualizations we make for everyone else</li>
        </ul>
    </div>
    <div class="col">
        <ul>
            <li class="fragment" data-fragment-index="2" style="list-style-type:none;">(The Teller)</li>
            <li class="fragment" data-fragment-index="3" style="list-style-type:none;">(The Tale)</li>
            <li class="fragment" data-fragment-index="4" style="list-style-type:none;">(The Told)</li>
        </ul>
    </div>
</div>

<div class="fragment" data-fragment-index="5">

Each of these brings with it different needs for **narrative**, for
**interactivity**, for **control** and for the **visual language** we use to convey
information.

</div>

<div class="fragment" data-fragment-index="5">

---

<div style="width: 640px; padding-top:5em;" data-markdown=true>
<h1>We tell lies to visualize.</h1>

<h3 style="text-align:right;">&mdash; Stuart Levy</h3>
</div>

---

<!-- .slide: data-background-image="https://upload.wikimedia.org/wikipedia/commons/b/bd/Kelvin_Helmholz_wave_clouds.jpg"
             data-background-size="cover" data-background-repeat="none" class="full" -->

<div class="multiCol">
<div class="col" data-markdown=true>
</div>
<div class="col fragment fade-in" style="opacity:0.7;background-color: white;" data-markdown=true>
$$\begin{aligned}{\partial \rho  \over \partial t}+\nabla \cdot (\rho \mathbf{v}) &= 0\\
{\frac {\partial \mathbf {v} }{\partial t}}+\mathbf {v} \cdot \nabla \mathbf {v} +{\frac {\nabla p}{\rho }}&=\mathbf {g}\\
{\partial e \over \partial t}+\mathbf {v} \cdot \nabla e+{\frac {p}{\rho }}\nabla \cdot \mathbf {v} &=0\end{aligned}$$
</div>
</div>

<!--<p class="mediumtext centered"><a href="https://commons.wikimedia.org/wiki/File:Kelvin_Helmholz_wave_clouds.jpg">Brocken Inaglory [CC BY-SA 4.0], via Wikimedia Commons</a></p> -->

---

<div class="multiCol">
<div class="col">
<div class="fig-container" data-style="height: 600px;" data-file="/2020-10-26-visastro-grammar-of-analysis/figures/kh_example.html" data-markdown=true>
</div>
</div>
<div class="col" data-markdown=true>
$$\begin{aligned}{\partial \rho  \over \partial t}+\nabla \cdot (\rho \mathbf{v}) &= 0\\
{\frac {\partial \mathbf {v} }{\partial t}}+\mathbf {v} \cdot \nabla \mathbf {v} +{\frac {\nabla p}{\rho }}&=\mathbf {g}\\
{\partial e \over \partial t}+\mathbf {v} \cdot \nabla e+{\frac {p}{\rho }}\nabla \cdot \mathbf {v} &=0\end{aligned}$$
</div>
</div>


---

## Mental Models of Data

<div class="multiCol">
<div class="col">

![Samantha Walkow](https://raw.githubusercontent.com/data-exp-lab/data-exp-lab.github.io/4ff6549d71c67b62b958fa6d8ff66c3dd2a13356/assets/img/people/swalkow.jpg) <!-- .element: class="headshot" -->

</div>

<div class="col">

Samantha Walkow has been conducting an investigation into "data storytelling" and how individual researchers describe their process.

Our understanding of the process of visualization, cognition, and semantically-meaningful models will outlast any single tool or platform.<!-- .element: class="fragment" -->

</div>
</div>

---

## The Data "Tour"

By focus on mutual learning, empowerment, and collaborative reflection, we center what participants choose to focus on and how they *conceptualize* the dataset.

What does the data mean to you, and how do you 'read' it?

---

## Phase One: Tell us about your data

<div class="multiCol">
<div class="col">

![Picture of a Disk](images/disk-filled-svgrepo-com.svg)

</div>
<div class="col">

The first step is asking the researcher to simply *tell* us about their data.
This is an unstructured process -- and it is not task based.  What *is* a
dataset to the researcher?

</div>
</div>

---

## Phase Two

<div class="multiCol">
<div class="col">
During the second phase, we ask three foundational questions.

<ul>
<li class="fragment">"What are the core, defining features of your data?"</li>
<li class="fragment">"What tools do you use to work with your data?"</li>
<li class="fragment">"How do you visualize your data?"</li>
</ul>

</div>
<div class="col">

![Question Mark](images/question-mark-svgrepo-com.svg)

</div>
</div>

---

## Phase Three:

We ask them to *draw* how they perceive data.

---

<div class="multiCol">
<div class="col">

![](images/s1_0.png)<!-- .element: class="storypanel fragment" -->

</div>
<div class="col">

![](images/s1_1.jpg)<!-- .element: class="storypanel fragment" -->

</div>
</div>
<div class="multiCol">
<div class="col">

![](images/s1_2.gif)<!-- .element: class="storypanel fragment" -->

</div>
<div class="col">

![](images/s1_3.png)<!-- .element: class="storypanel fragment" -->

</div>
</div>

---

<div class="multiCol">
<div class="col">

![](images/s2_0.png)<!-- .element: class="storypanel fragment" -->

</div>
<div class="col">

![](images/s2_1.png)<!-- .element: class="storypanel fragment" -->

</div>
</div>
<div class="multiCol">
<div class="col">

![](images/s2_2.png)<!-- .element: class="storypanel fragment" -->

</div>
<div class="col">

&nbsp;

</div>
</div>

---

<div class="multiCol">
<div class="col">

![](images/s3_0.png)<!-- .element: class="storypanel fragment" -->

</div>
<div class="col">

![](images/s3_1.png)<!-- .element: class="storypanel fragment" -->

</div>
</div>
<div class="multiCol">
<div class="col">

![](images/s3_2.png)<!-- .element: class="storypanel fragment" -->

</div>
<div class="col">

&nbsp;

</div>
</div>

---

## Our Data Stories

How we tell our stories is impacted greatly by how we learn, and how data practices are handed down to us.

---

## Our Data Stories

<div class="multiCol">
<div class="col">

![Network Transmission](images/network-transmit-receive-svgrepo-com.svg)

</div>
<div class="col">
Data practices are culturally transmitted.
</div>
</div>

---

## Our Data Stories

<div class="multiCol">
<div class="col">
Linking and layering of information is driven by a search for causality.
</div>
<div class="col">

![Layers](images/layer-svgrepo-com.svg)

</div>
</div>

---

## Our Data Stories

<div class="multiCol">
<div class="col">

![World](images/world-svgrepo-com.svg)

</div>
<div class="col">
Data practices are embedded in broader cultural and social practices around technology.
</div>
</div>

---

# Our Data Stories

* Character
* Setting
* Plot

As researchers, we can map our data onto these narrative elements.

<p class="fragment">We must also take into account our role in the presentation; we bring unique motivation, style and methods to our storytelling.</p>

<p class="fragment">We can codify this in our presentation of our visualizations.</p>

---

# Why are we telling this story?

What is our motivation for presenting this information?  There can be many, and they are not necessarily advertised in the *text* of your tale.  You may find that the three types of story we have described map to one or more of these categories more frequently than others.

<p class="fragment">What are some reasons and contexts you anticipate telling a data story?</p>

<p class="fragment">Who might be in your audience?</p>

<p class="fragment">What is your relationship with them?</p>

---

# Why: Persuasion

Are you leading your audience to a conclusion?  What are some instances in which your primary motivation is to persuade someone of a piece of information?

<p class="fragment">What are different <i>levels</i> of conclusion that you might want to reach in a research setting?</p>

---
 
# Why: Collaborative Thinking
 
Perhaps your motivation behind telling the tale is to develop a collaborative discussion, and to present it as an unknown.

<p class="fragment">(Or maybe you just want it to seem like you're collaborating, but really you're leading?)</p>

<p class="fragment">How might you structure your talk, and choose what you do and do not include?</p>

---

# Why: To Tell a Tale
 
Sometimes telling a tale is just to tell it, to provide voice to information.

<p class="fragment">Sometimes we tell a tale without knowing <i>why</i> we tell it, at first, and we discover later.</p>

<p class="fragment">"Maybe the <i>real</i> treasure was the friends we made along the way."</p>

---

# How are we telling the story?

If we define a single piece of information, or a "state" in between transitions (slides, narrative, visual, or otherwise) we can think of how we navigate between those as falling into a few different categories.

<p class="fragment">This is not a <i>full</i> ontology of how to navigate, but it does touch on a few methods that are approachable.</p>

---

# How: Narrative Progression

The most straightforward approach to telling your data story is to identify a variable, and move along that variable.

<p class="fragment">Is that variable always time?  What other variables might there be?</p>

<p class="fragment">Are we moving monotonically?  Do we move at a fixed rate?  How do we ensure adequate information coverage?</p>

---

# How: Expansion of Components

We can *not* present all of the information in a narrative.  But, we can selectively expand on individual components.  For instance, you might choose individual items, "zoom" in on them and [describe them in detail](https://youtu.be/r7Eq3Hr0ehw?t=1595).

<p class="fragment">We see this with maps pretty often.</p>

<p class="fragment">What coverage do we want of the items we can present?  How do we choose our illustrative examples, and how is that informed by our motivations?</p>

---

# How: Non-linear Exploration

Perhaps we have no direction for describing -- we have many variables, many directions, or perhaps the variables are not as well defined?

<p class="fragment">How do you choose what to visit first?  What does 'visiting' an informational node mean in this context?</p>

<p class="fragment">

---

# How: Your Style

How controlling of the narrative process are you?

<p class="fragment">Are you an auteur, personally influencing not only the presentation but the journey for your audience?</p>

<p class="fragment">Do you have the opportunity to allow freedom of exploration?  How restrictive?  Where does the technology limit you?</p>

<p class="fragment">How reliant on appeals to emotion, empathy, relatedness or intuition is your data story?</p>

---

# Wrapping Up

How can we take these different aspects of the "why" and the "how" of our storytelling and construct our stories?

More specifically, how can we identify different *classes* of data that fall easily into these different models?

---

# Thank You

Thank you for this opportunity to talk with you today, and I look forward to
getting to hear the rest of the speakers!
