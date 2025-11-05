<style type="text/css">
.black {
  color: black;
}
.inline-left {
  display: inline-block;
  text-align: left;
}
.reveal ul {
  margin: 0;
}
</style>

<div style="font-size: 300%; font-weight: 600;">
Veridical Data Science
</div>

<br/>
<div style="font-size: 180%; font-weight: 600;">
Scientific Python, the Berkeley OSPO, and BIDS
</div>

<br/>
<br/>
<br/>


<div style="display: flex; justify-content: center; margin-left: 2em;">
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="150em"/>
<img alt="Scientific Python logo" src="images/dancing-logo-berkeley.svg" style="margin-left: 6em;"/>
<img alt="Berkeley OSPO logo" src="images/BIDS-logo.svg" width="210em" style="margin-left: 6em;"/>
</div>

<!--
### Why?
### How?
### What?
-->

<br/>
<br/>
<br/>
<br/>

---

# Motivation & History

...

<img src="images/bic.png" />

Notes:

- Lab created code, personal scripts, home-developed infrastructure (e.g., job scheduler)
- Scripts and libraries written in multiple languages
  (IDL, Matlab, C, Perl, Awk, etc.)
- Pushed the limits of existing hardware
- Switching from proprietary Unix to Linux

...

<img src="images/fmri.jpg" />

Source: Wikipedia

...

<img src="images/fmri-pipeline.png" width="800em" />

Source: Martin A. Lindquist, "The Statistical Analysis of fMRI Data" (2008)

...

# Barriers

- hodgepodge of languages
- lab-specific, machine-specific, sequence-specific code
- no standard file layout, naming conventions
- limited public code and data repositories
- limited online collaborative tooling

...

# Can we do better?

...

<img src="images/redhat.jpg"  width="50%" />

...

<img src="images/wavelab.png" width="80%" />

...

<img src="images/python-logo.png" width="80%" />

...

<img src="images/nipy.svg"/>

<div style="color: darkgray;">

> We believe that neuroscience <span class="black">ideas and analysis develop
> together</span>.
> Good ideas come from understanding; <span class="black">understanding comes
> from clarity</span>, and <span class="black">clarity must come from</span> well-designed teaching
> materials and <span class="black">well-designed software</span>.
> The <span class="black">software must be</span> designed
> as <span class="black">a natural extension of the underlying ideas</span>.
>
http://nipy.org/nipy/mission.html

</div>

...

## A Spark At Berkeley

### 2003–2012

<img src="images/team.png" width="80%" />

Notes:

- Python not serious alternative to Matlab / IDL
- 04 meet FP, JT, JH, TP, PG, et al
- 05 course Tolman Hall by FP and JH
- 08 Fernando appointed at the BIC
- 10 SciPy India. meet Stéfan, US SciPy conference proceedings
- Josh Bloom, Python bootcamp, AY250

...

<img src="images/cise2007-cover.png" width="49%" />
<img src="images/cise2007-toc.png" width="39%" />

...

<img src="images/cise2011-cover.png" width="49%" />
<img src="images/cise2011-toc.png" width="49%" style="padding-bottom: 4rem;" />

...

<div style="color: darkgray;">

> In 2024,  <span class="black">Python</span> overtook JavaScript as the  <span class="black">most popular language</span> on GitHub,
> while Jupyter Notebooks skyrocketed—both of which underscore the surge in <span class="black">
> data science and machine learning</span> on GitHub.

</div>

https://github.blog/news-insights/octoverse/octoverse-2024/

Notes:

- the Data Science curriculum is launched, built around Python.
- statistical computing taught in Python

---

# Veridical Data Science

...

<img src="images/vds-workshop.png"  />

https://www.youtube.com/@UCBIDS

...

> There is increasing concern that in modern research, **false findings may be the majority or even the vast majority** of published research claims.
However, this should not be surprising.
It can be proven that most claimed research ﬁndings are false.

John P. A. Ioannidis, "Why Most Published Research Findings Are False" (2005)

Notes:

- The paper uses mathematical modeling to show that even without any bias, the probability that a research claim is true (the positive predictive value) is often less than 50% for most study designs.
- Study design and power: Smaller study sizes and smaller effect sizes increase the likelihood of false positives.
- Flexibility and bias: Flexibility in designs, definitions, and analytical modes allows researchers to massage data until a significant result appears.
- Selective reporting: Focusing on a single positive result while ignoring others, a practice known as "cherry picking," leads to unreliable findings.
- Research environment: A competitive environment where speed is prioritized over rigor, along with vested interests, can contribute to more false findings.
- Lack of replication: A lack of independent replication of results makes it harder to confirm initial findings.

...

<img src="images/three_realms.png" width="80%" />

https://vdsbook.com/#what-is-veridical-data-science

...

## Data Science Life Cycle (DSLC)

<br/>

1. Problem Formulation / Data Collection
2. Data Cleaning and EDA
3. Data Preparation
4. Predictions and Inference
5. Evaluation of Results
6. Communication of Results

<img src="images/fmri-pipeline.png" width="250em" style="margin-left: 2em;" />

Notes:

The DSLC is iterative and non-linear---you frequently return to refine earlier stages.


1. Problem Formulation and Data Collection
   - Translate domain problems into data science questions
   - Ensure data relevance and quality

2. Data Cleaning and Exploratory Data Analysis (EDA)
   - Handle missing values, outliers, inconsistencies
   - Understand data structure and patterns

3. Uncovering Intrinsic Data Structures
   - Dimensionality reduction
   - Clustering and pattern discovery

4. Predictions and Inference
   - Build and compare multiple models
   - Evaluate on held-out test data

5. Evaluation of Results
   - Scrutinize findings; assess validity
   - Guard against confirmation bias

6. Communication of Results
   - Present findings clearly to domain audiences
   - Document all decisions and justifications

...

## Multiple Valid Paths, Different Outcomes

<br/>

- Each step in the data science life cycle requires judgment calls
- Different but reasonable choices lead to different analytical paths and conclusions
- Traditional statistical frameworks fail to account for uncertainty from these choices
- Researchers can take many different analytical paths when wrangling, analyzing, and interpreting data

Notes:

This is not about misconduct---it is about the **inherent complexity of scientific analysis**.

...

# Can we do better?

...

## The PCS Framework

Yu and Kumbier, PNAS (2000)


Notes:

**Unifying principle:** Aggregate multiple reasonable analytical approaches

- as good doctors would aggregate opinions on a serious diagnosis

...

## Summary and Key Takeaways

<br/>

Reproducibility and reliability require **systematic attention to human judgment calls** throughout the entire DSLC, not just careful data collection or statistical testing.

<br/>

**Core framework (PCS)**
- **Predictability:** Reality check---do results predict well on new data?
- **Computability:** Tractability and transparency of analytical pipeline
- **Stability:** Robustness to reasonable perturbations at every DSLC stage

Notes:

Predictability

- Ensures the DSLC captures reality and addresses the domain problem
- Results must predict well on held-out or future data
- Validates that conclusions align with domain knowledge

Answers: Does this actually work in the real world?

Computability

- Ensures analytical choices are computationally tractable and scalable
- Considers data collection, storage, and algorithm efficiency
- Includes data-inspired simulations (MERITS, simChef)

Answers: Can we actually execute and replicate this analysis?

Stability

- Most important principle for addressing judgment calls
- Tests whether results hold under reasonable changes to data and methods
- Expands traditional robustness concepts across entire DSLC

Answers: Do conclusions remain robust to alternative (but reasonable) decisions?

...

## Practical Considerations

1. Data Management
2. Algorithm Selection
3. Workflow Automation
4. Version Control and Infrastructure
5. Documentation

Notes:

1. Data Management:
   - Efficient storage and retrieval
   - Scalability to large datasets
   - Version control for data provenance

2. Algorithm Selection:
   - Efficiency and computational complexity
   - Feasibility on available resources
   - Ability to scale for production deployment

3. Workflow Automation:
   - Use make, Snakemake, or workflow systems to automate analytical pipelines
   - Record dependencies between data, code, and outputs
   - Enable reproducible re-execution

4. Version Control and Infrastructure:
   - Git for tracking code evolution
   - Automated testing to catch errors early
   - Continuous integration/deployment

5. Documentation:
   - Literate computing approach (Jupyter Notebooks, R Markdown)
   - Combine narratives, code, and visualizations
   - Justify each judgment call in context

...

## Looking forward

- Implement PCS framework in widely-used OSS
- Integrate generative AI responsibly with PCS principles
- Expand veridical data science across scientific domains
- Build institutional practices supporting trustworthy research culture

---

# Questions

---

# Scientific Python

...

<img src="images/python-stack.png"  />

https://jupytearth.org/jupyter-resources/introduction/ecosystem.html

...

<img src="images/ecosystem.png" width="70%" />

https://www.nature.com/articles/s41586-020-2649-2

...

<img src="images/arrays.png" width="70%" />

...

<img src="images/array-programming.png" />

https://www.nature.com/articles/s41586-020-2649-2

...

<img src="images/scikithep-scip.png" />

https://www.argmin.net/p/the-higgs-discovery-did-not-take

Notes:

- Matthew Feickert
- Henry Schreiner 
- Jim Pivarski

...

<img src="images/python-stack.png"  />

...

<img src="images/shells-hep.svg"  width="80%"   />

...

## Principles

<br/>

- community developed, and community owned
- transparent, open
- intuitive & expressive

<!--
  - transparent, open (distribute and modify—user contributer)
  - aligned incentives (vs commercial, e.g.)
  - paves way towards reproducible research
-->

<!--
- importance of language and library choices
-->

<!--
- general-purpose
  - prioritizes human (not computer) time
-->

Notes:

- This is the best way to align incentives for doing good quality, transparent, reproducible science
- We believe that researchers know their needs best
- Their ideas must be surfaced and integrated into the computational
  platform as efficiently as possible
- In this endeavor, making money for shareholders is at best a
  distraction
  - But often, it incentivises entirely the wrong things: hardware
    locks, license servers, closed file formats
  - Incentive to lock users into  proprietary systems
    - This prohibits sharing, reproducibility, and transparency

- Transparency: you *should* always be able to investigate the
  *entire* scientific stack.
- To know answers are accurate, you have to be able to look under the
  hood.
- You also need to be able to modify tools to do *new things*, to do
  *whatever* needs to be done.
- The change required is bigger than just open software; you need
  reproducible research as well (i.e. data/methods publishing). But
  it's a start.

- The **importance of language and library choices** cannot be underestimated.

- General-purpose
- Readable code
- Prioritize human (not computer) time

- Re-emphasises the notion of a user-developer
- Library interfaces and language clarity / expressivity matter: it's
  how we express our thoughts.

...

## Practices I

<img src="images/practice.png"/>

http://www.jarrodmillman.com/publications/millman2014developing.pdf

Notes:

**Technical**

- Revision control
- Testing / continuous integration
- Code review
- Documentation
- Iteration

**Social**

- Governance and Coordination

No matter how sound philosophy, we still need working code!

Code review both during development cycle, but also during use where
users can easily introspect for problems. -->

<!-- Documentation has to stay in sync with code (docstrings). -->

...

## Practices II

#### Stat 159/259 Fall 2015

<img src="images/stat159-2015.png" width="80%" />

...

## People

<img src="images/community.png"/>

<br/>


Notes:

- Work done in collaboration is better and more fun.

  - **Community** is meaningful.
  - **Culture** is important for good work.
  - **Leadership** sets direction.
  - **Governance** sets expectations and reduces misunderstandings.

- Community

  - Many of my best friends I made through this ecosystem.

  - These have been the most fulfilling and educational collaborations
    of my life.

  - Being part of a movement where everyone is aligned is incredibly
    exciting.

  - For me, personally, it's been transformative to my career. Lots of
    people have helped me get where I am today.

- Culture

  - In a volunteer effort you cannot afford *not* to treat people
    well

  - Unsurprisingly, when people feel welcome, listened to, engaged, they produce
    better work

- Leadership

  - It helps greatly when the founders of projects set the right tone;
    one of the things that drew me into SP from the beginning

    - Various projects had you earn your badge
    - SP phone call from Berkeley: trust placed in newcomers,
      welcomed with open arms, treated with respect (listen to opinions)

...

## Problems

...  sustained by independent volunteers with separate
mailing lists, websites, roadmaps, documentation, engineering and
packaging solutions, and governance structures.

- duplicated effort
- disorganized documentation
- breakage upon new releases
- unintended performance regressions
- user confusion
- no shared vision of the future

...

# Can we do better?

...

<img src="images/home.png" width="90%"/>

...

<img src="images/specs.png" />

...

## SPEC 0

<img src="images/support-window.png" />

...

## SPEC 4

<img src="images/nightly.png" />

...

<img src="images/summits.png" width="75%"/>

...

<img src="images/fourth-summit.jpg" width="75%"/>

...

<img src="images/devguide.png" width="75%"/>

https://learn.scientific-python.org/development/

...

<img src="images/cookie-star-history.png" />

...

<img src="images/statistical-python.png" />

---

# Open Source Program Office

...

# Mission

> to facilitate knowledge sharing, promote best practices, and provide support for open-source projects at every stage of their lifecycle. Whether you’re a seasoned developer, a curious student, or an academic seeking to leverage open-source tools, we’re here to provide resources, guidance, and opportunities for engagement.

...

# Events

- Thursday, November 6 @ 10am (online) - OSPO Monthly Knowledge Exchange: JupyterCon Share Out

- Thursday, November 20 @ 3:30pm (hybrid) - OSPO Monthly Meetup: Monica Bobra, Principal Data Scientist at the California Office of Data and Innovation

- Thursday, December 4 @ 10am (online) - OSPO Monthly Knowledge Exchange

https://bids.berkeley.edu/programs-initiatives/open-source-program-office-ospo

...

# Connect with us

- Join us on Slack!

<div style="display: flex; justify-content: center; margin-left: 2em;">
<img alt="Scientific Python logo" src="images/qr-code.png" width="230em"/>
</div>

- Email us at ospo+subscribe@lists.berkeley.edu to join our mailing list

---

# Questions

---

# Extra slides

...

## Predictability (P)

<br/>


- Ensures the DSLC captures reality and addresses the domain problem
- Results must predict well on held-out or future data
- Validates that conclusions align with domain knowledge

Answers: Does this actually work in the real world?

Notes:

Reality Check

...

## Computability (C)

<br/>


- Ensures analytical choices are computationally tractable and scalable
- Considers data collection, storage, and algorithm efficiency
- Includes data-inspired simulations (MERITS, simChef)

Answers: Can we actually execute and replicate this analysis?

Notes:

- Ensures analytical choices are computationally tractable and scalable

...

## Stability (S)

<br/>

- Most important principle for addressing judgment calls
- Tests whether results hold under reasonable changes to data and methods
- Expands traditional robustness concepts across entire DSLC

Answers: Do conclusions remain robust to alternative (but reasonable) decisions?

Notes:

Reproducibility Through Perturbation Analysis

...

## Computability

Practical Considerations

1. Data Management
2. Algorithm Selection
3. Workflow Automation
4. Version Control and Infrastructure
5. Documentation

Notes:

1. Data Management:
   - Efficient storage and retrieval
   - Scalability to large datasets
   - Version control for data provenance

2. Algorithm Selection:
   - Efficiency and computational complexity
   - Feasibility on available resources
   - Ability to scale for production deployment

3. Workflow Automation:
   - Use make, Snakemake, or workflow systems to automate analytical pipelines
   - Record dependencies between data, code, and outputs
   - Enable reproducible re-execution

4. Version Control and Infrastructure:
   - Git for tracking code evolution
   - Automated testing to catch errors early
   - Continuous integration/deployment

5. Documentation:
   - Literate computing approach (Jupyter Notebooks, R Markdown)
   - Combine narratives, code, and visualizations
   - Justify each judgment call in context
   
...
 
## Summary and Key Takeaways II

**Practical implications**
- Document decisions and explore alternatives, not just report final answer
- Use multiple models and ensemble approaches rather than single optimum
- Conduct stability analysis across data cleaning, preprocessing, and modeling choices
- Report uncertainty honestly through prediction intervals and confidence ranges

**For collaborative research**
- Clear documentation enables team understanding and code review
- Version control and automation support reproducibility
- Open practices build trust and enable external validation

**Looking forward**
- Integrate generative AI responsibly with PCS principles
- Expand veridical data science across scientific domains
- Develop theoretical foundations for connections among PCS principles
- Build institutional practices supporting trustworthy research culture

