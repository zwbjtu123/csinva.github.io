- 3 types
	- disease and patient categorization (e.g. classification)
	- fundamental biological study
	- treatment of patients
- philosophy
  - want to focus on problems doctors can't do
  - alternatively, focus on automating problems parents can do to screen people at home in cost-effective way
- websites are often easier than apps for patients
- [challenges in ai healthcare (news)](https://www.statnews.com/2019/06/19/what-if-ai-in-health-care-is-next-asbestos/)
  - adversarial examples
  - things can't be de-identified
  - algorithms / data can be biased
  - correlation / causation get confused

# evaluation

- doctors are evaluated infrequently (and things like personal traits are often included)
- US has pretty good care but it is expensive per patient
- expensive things (e.g. Da Vinci robot)
- even if ml is not perfect, it may still outperform some doctors



# how do doctors think

- doctors also misinterpret things to be causal
- doctors don't have intuition for even relatively simple features, such as averages
- doctors require context for features (e.g. this feature is larger than the average)
- often have some rules memorized (otherwise memorize what needs to be looked up)
  - unclear how well doctors follow rules
  - some rules are 1-way (e.g. only follow it if it says there is danger, otherwise use your best judgement)
    - 2-way rules are better
    - without proper education 1-way rules can be dangerously used as 2-way rules
    - doesn't make sense to judge 1-way rules on both sepcificity and sensitivity
- rules are often ambiguous (e.g. what constitutes vomiting)
- **doctors adapt to personal experience** - may be unfair to evaluate them on larger dataset
- sometimes said that doctors know 10 medications by heart
- [Overconfidence in Clinical Decision Making](https://www.amjmed.com/article/S0002-9343(08)00152-6/pdf)
  - most uncertainty: family medicine [FM] and emergency medicine [EM]
  - some uncertainty: internal medicine
  - little uncertainty: specialty disciplines
  - 2 systems at work: intuitive (uses context, heuristics) vs analytic (systematic, rule-based)
    - a combination of both performs best
  - doctors are often black boxes as well - validated infrequently, unclear how closely they follow rules
  - doctors adapt to local conditions - should be evaluated only on local dataset

# doctor education

- rarely textbooks (often just slides)
- 1-2% miss rate for diagnosis can be seen as acceptable
- [how doctors think](https://www.newyorker.com/magazine/2007/01/29/whats-the-trouble)
  - 2 years: memorizing facts about physiology, pharmacology, and pathology
  - 2 years learning practical applications for this knowledge, such as how to decipher an EKG and how to determine the appropriate dose of insulin for a diabetic
  - little emphasis on metal logic for making a correct diagnosis and avoiding mistakes
  - see work by pat croskerry
  - there is limited data on misdiagnosis rates
  - **representativeness** error - thinking is overly influenced by what is typically true
  - **availability** error - tendency to judge the likelihood of an event by the ease with which relevant examples come to mind
    - common infections tend to occur in epidemics, afflicting large numbers of people in a single community at the same time
    - confirmation bias
  - **affective** error - decisions based on what we wish were true (e.g. caring too much about patient)
  - See one, do one, teach one - teaching axiom

# political elements

- [why doctors should organize](https://www.newyorker.com/culture/annals-of-inquiry/why-doctors-should-organize)
- big pharma
- day-to-day
  - Doctors now face a burnout epidemic: thirty-five per cent of them show signs of high depersonalization
  - according to one recent [report](https://jamanetwork.com/journals/jamainternalmedicine/fullarticle/2730353?resultClick=1), only thirteen per cent of a physician’s day, on average, is spent on doctor-patient interaction
  - [study](https://www.nytimes.com/2017/11/14/well/live/the-patients-vs-paperwork-problem-for-doctors.html) during an average, eleven-hour workday, six hours are spent at the keyboard, maintaining electronic health records.
  - medicare's r.v.u - changes how doctors are reimbursed, emphasising procedural over cognitive things
  - ai could help - make simple diagnoses faster, reduce paperwork, help patients manage their own diseases like diabetes
  - ai could also make things worse - hospitals are mostly run by business people

# terminology

- internal/external validity = training/testing error

# medical ai example

- EKG has a small interpretation on it
- there used to be bayesian networks / expert systems but they went away...

# icu interpretability example

- goal: explain the model not the patient (that is the doctor’s job)
- want to know interactions between features
- some features are difficult to understand
  - e.g. max over this window, might seem high to a doctor unless they think about it
- some features don’t really make sense to change (e.g. was this thing measured)
- doctors like to see trends - patient health changes over time and must include history
- feature importance under intervention

# communicating findings

- [don't use ROC curves, use deciles](https://modelplot.github.io/intro_modelplotpy.html)
- [need to evaluate use, not just metric](https://jamanetwork.com/journals/jama/fullarticle/2748179)