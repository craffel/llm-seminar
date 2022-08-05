# COMP790-101: Large Language Models

Instructor: [Colin Raffel](http://colinraffel.com)

Meeting time: Mondays and Wednesdays, 1:25-2:40pm

Classroom: SN 011

Office hours: By appointment

Language models, which are trained to predict text given other text, underly many recent successes in natural language processing and artificial intelligence.
Whether used for transfer learning (using language modeling as a pre-training objective before subsequent fine-tuning on a downstream task) or prompting (formulating an input sequence that induces a model to perform a desired task without any training), language modeling has proven to be an effective way of imbuing models with useful capabailities.
These capabilities have been observed to consistently improve as the size of the language model increases, which has led to a focus on developing ever-larger language models.
In this course, we will survey the history of language model scaling, as well as recent advances in building, analyzing, and using large LMs.
The course will use a [role-playing seminar format](https://colinraffel.com/blog/role-playing-seminar.html), described in more detail below.

## Prerequisites

Students must have experience with machine learning (preferably deep learning) and the basics of modern natural language processing.
Before taking the class, you should be able to read a recent machine learning or natural language processing conference paper and come away with a decent understanding of the basic concepts and ideas proposed in the paper (but not necessarily a deep, perfect understanding of every last detail).

## Course Structure

This class will use a [role-playing seminar](https://colinraffel.com/blog/role-playing-seminar.html) format where students take on different roles and present papers to one another.
All grading will be based on these presentations and course participation; there will be final project or other coursework.

### Readings

Each class will involve the presentation and discussion of two papers.
The pair of papers covered in each class session are meant to complement each other, e.g. because one paper might be the historical precedent of the other, or the papers were contempraneous, or they present different viewpoints on the same topic.
Before each class, everyone is required to have read both papers.
Students will be divided into four groups.
Two groups will present on Mondays and the other two groups will present on Wednesdays.
In a given class session, students in the presenting groups will each be given a rotating role (described below).
This role defines the lens through which they read the paper and determines what they prepare for the in-class discussion.
Students in the non-presenting groups are also required to read the papers, complete a quick exercise (described below), and come to class ready to discuss.
All students will obtain a thorough understanding of the chosen papers and will develop their paper reading, literature review, and prototyping skills.

#### Presentation roles

This seminar is organized around the different "roles" students play each week:
Reviewer, Archaeologist, Researcher, Hacker, and (possibly) Private Investigator.

  - **Reviewer:** Complete a full---critical but not necessarily negative---review of the paper. Follow the [guidelines for NeurIPS reviewers](https://nips.cc/Conferences/2020/PaperInformation/ReviewerGuidelines) (under "Review Content"), taking note of the example reviews included therein, *except* you should *not* summarize the paper, since everyone in the class will already have read it. In particular, please answer questions 1 to 10 under "Review Content", including assigning an overall score.
  - **Archaeologist:** Determine where this paper sits in the context of previous and subsequent work. Find and report on one prior paper *that we are not reading in this class* that substantially influenced the current paper and one newer paper *that we are not reading in this class* that cites this current paper.
  - **Researcher:** Propose an imaginary follow-up project -- not just based on the current but only possible due to the existence and success of the current paper.
  - **Hacker:** Implement a small part of the paper on a small dataset or toy problem. Prepare to share the core code of the algorithm to the class. Do not simply download and run an existing implementation - you should implement at least a (toy version of a) method from the paper, though you are welcome to use (and give credit to) an existing implementation for "backbone" code (e.g. model building, data loading, training loop, etc.).
  - (optionally, depending on course enrollment) **Private Investigator:** Find out background information on one of the paper authors. Where have they worked? What did they study? What previous projects might have led to working on this one? What do you think motivated them to work on this project? Feel free to contact the authors, but remember to be courteous, polite, and on-topic. Write that you're in Prof. Raffel's seminar and include a link to this page.

#### Non-presenter assignment

If you aren't in the presenting group during a given class period, please come to class with *both*:
  1. A new title for the paper and/or a new name for the algorithm it proposes
  1. At least one question about the paper (either something you're confused about or something you'd like to hear discussed more)

## Schedule

The schedule below includes a preliminary list of the papers we will be reading.
These papers are subject to change, though I will try to make changes only to papers that are at least two weeks away.
If you have any suggested changes, feel free to tell me.

|    Date    |                                                                               Group A Paper                                                                               |                                                                                             Group B paper                                                                                             |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  Mon, 8/15 | Class introduction, background, logistics                                                                                                                                 | N/A                                                                                                                                                                                                   |
|  Wed, 8/17 | [Attention Is All You Need](https://arxiv.org/abs/1706.03762) (Colin presents)                                                                                            | N/A                                                                                                                                                                                                   |
|  Mon, 8/22 | [Generating Sequences With Recurrent Neural Networks](https://arxiv.org/abs/1308.0850)                                                                                    | [The Unreasonable Effectiveness of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/)                                                                                |
|  Wed, 8/24 | [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473)                                                                  | [Exploring the Limits of Language Modeling](https://arxiv.org/abs/1602.02410)                                                                                                                         |
|  Mon, 8/29 | [Semi-supervised Sequence Learning](https://arxiv.org/abs/1511.01432)                                                                                                     | [Learning to Generate Reviews and Discovering Sentiment](https://arxiv.org/abs/1704.01444)                                                                                                            |
|  Wed, 8/31 | [Universal Language Model Fine-tuning for Text Classification](https://arxiv.org/abs/1801.06146)                                                                          | [Improving Language Understanding by Generative Pre-Training](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)                |
|   Mon, 9/5 | No class (Labor Day)                                                                                                                                                      | N/A                                                                                                                                                                                                   |
|   Wed, 9/7 | [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805)                                                      | [RoBERTa: A Robustly Optimized BERT Pretraining Approach](https://arxiv.org/abs/1907.11692)                                                                                                           |
|  Mon, 9/12 | [ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators](https://arxiv.org/abs/2003.10555)                                                          | [DeBERTa: Decoding-enhanced BERT with Disentangled Attention](https://arxiv.org/abs/2006.03654)                                                                                                       |
|  Wed, 9/14 | [Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer](https://arxiv.org/abs/1910.10683)                                                     | [Unified Language Model Pre-training for Natural Language Understanding and Generation](https://arxiv.org/abs/1905.03197)                                                                             |
|  Mon, 9/19 | [Cross-lingual Language Model Pretraining](https://arxiv.org/abs/1901.07291)                                                                                              | [ByT5: Towards a token-free future with pre-trained byte-to-byte models](https://arxiv.org/abs/2105.13626)                                                                                            |
|  Wed, 9/21 | [Language Models are Unsupervised Multitask Learners](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) | [Language Models are Few-Shot Learners](https://arxiv.org/abs/2005.14165)                                                                                                                             |
|  Mon, 9/26 | No class (well-being day)                                                                                                                                                 | N/A                                                                                                                                                                                                   |
|  Wed, 9/28 | [Scaling Laws for Neural Language Models](https://arxiv.org/abs/2001.08361)                                                                                               | [Training Compute-Optimal Large Language Models](https://arxiv.org/abs/2203.15556)                                                                                                                    |
|  Mon, 10/3 | [Scaling Language Models: Methods, Analysis & Insights from Training Gopher](https://arxiv.org/abs/2112.11446)                                                            | [PaLM: Scaling Language Modeling with Pathways](https://arxiv.org/abs/2204.02311)                                                                                                                     |
|  Wed, 10/5 | [On the Dangers of Stochastic Parrots: Can Language Models Be Too Big? 🦜](https://dl.acm.org/doi/10.1145/3442188.3445922)                                                 | [Release Strategies and the Social Impacts of Language Models](https://arxiv.org/abs/1908.09203)                                                                                                      |
| Mon, 10/10 | [RealToxicityPrompts: Evaluating Neural Toxic Degeneration in Language Models](https://arxiv.org/abs/2009.11462)                                                          | [Documenting Large Webtext Corpora: A Case Study on the Colossal Clean Crawled Corpus](https://arxiv.org/abs/2104.08758)                                                                              |
| Wed, 10/12 | [Extracting Training Data from Large Language Models](https://arxiv.org/abs/2012.07805)                                                                                   | [Deduplicating Training Data Makes Language Models Better](https://arxiv.org/abs/2107.06499)                                                                                                          |
| Mon, 10/17 | [Language Models as Knowledge Bases?](https://arxiv.org/abs/1909.01066)                                                                                                   | [REALM: Retrieval-Augmented Language Model Pre-Training](https://arxiv.org/abs/2002.08909)                                                                                                            |
| Wed, 10/19 | [Exploiting Cloze Questions for Few Shot Text Classification and Natural Language Inference](https://arxiv.org/abs/2001.07676)                                            | [The Power of Scale for Parameter-Efficient Prompt Tuning](https://arxiv.org/abs/2104.08691)                                                                                                          |
| Mon, 10/24 | [Defending Against Neural Fake News](https://arxiv.org/abs/1905.12616)                                                                                                    | [CTRL: A Conditional Transformer Language Model for Controllable Generation](https://arxiv.org/abs/1909.05858)                                                                                        |
| Wed, 10/26 | [Multitask Prompted Training Enables Zero-Shot Task Generalization](https://arxiv.org/abs/2110.08207)                                                                     | [Benchmarking Generalization via In-Context Instructions on 1,600+ Language Tasks](https://arxiv.org/abs/2204.07705)                                                                                  |
| Mon, 10/31 | [Exploring and Predicting Transferability across NLP Tasks](https://arxiv.org/abs/2005.00770)                                                                             | [Don't Stop Pretraining: Adapt Language Models to Domains and Tasks](https://arxiv.org/abs/2004.10964)                                                                                                |
|  Wed, 11/2 | [Training language models to follow instructions with human feedback](https://arxiv.org/abs/2203.02155)                                                                   | [Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2204.05862)                                                                         |
|  Mon, 11/7 | [How Many Data Points is a Prompt Worth?](https://arxiv.org/abs/2103.08493)                                                                                               | [Do Prompt-Based Models Really Understand the Meaning of their Prompts?](https://arxiv.org/abs/2109.01247)                                                                                            |
|  Wed, 11/9 | [Calibrate Before Use: Improving Few-Shot Performance of Language Models](https://arxiv.org/abs/2102.09690)                                                               | [Rethinking the Role of Demonstrations: What Makes In-Context Learning Work?](https://arxiv.org/abs/2202.12837)                                                                                       |
| Mon, 11/14 | [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://arxiv.org/abs/1701.06538)                                                       | [Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity](https://arxiv.org/abs/2101.03961)                                                                      |
| Wed, 11/16 | [Learning Transferable Visual Models From Natural Language Supervision](https://arxiv.org/abs/2103.00020)                                                                 | [🦩 Flamingo: a Visual Language Model for Few-Shot Learning](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/tackling-multiple-tasks-with-a-single-visual-language-model/flamingo.pdf) |
| Mon, 11/21 | [Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM](https://arxiv.org/abs/2104.04473)                                                       | [DeepSpeed: Extreme-scale model training for everyone](https://www.microsoft.com/en-us/research/blog/deepspeed-extreme-scale-model-training-for-everyone/)                                            |
| Wed, 11/23 | No class (Thanksgiving break)                                                                                                                                             | N/A                                                                                                                                                                                                   |
| Mon, 11/28 | [GLUE: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding](https://arxiv.org/abs/1804.07461)                                                 | [Beyond the Imitation Game: Quantifying and extrapolating the capabilities of language models](https://arxiv.org/abs/2206.04615)                                                                      |
| Wed, 11/30 | [GPT-NeoX-20B: An Open-Source Autoregressive Language Model](https://arxiv.org/abs/2204.06745)                                                                            | [OPT: Open Pre-trained Transformer Language Models](https://arxiv.org/abs/2205.01068)                                                                                                                 |
|  Sat, 12/3 | (reserved for late-breaking paper)                                                                                                                                        | (reserved for late-breaking paper)                                                                                                                                                                    |

## Grading

1. Presentations (84 points): For each class session where you are presenting, you will be graded out of 6 points. You will receive full credit if you do a thorough job of undertaking your role and present it in a clear and compelling way.
1. Participation (14 points): For each class session where you aren't presenting, you'll be given up 1 point for completing the non-presenter assignment and attending and participating in class.
1. Free points (2 points): All students get 2 free points!

## Attendance, late work, and the honor code

If you miss a class without completing the corresponding assignment, you'll get a zero for that session.
If you miss a class where you are in a "presenting" role for that session, you must still create the presentation for that role before the class and you must find someone else to present it for you.
If you miss a class where you'd be in a "non-presenting" role, to get credit for that session you need to complete the non-presenting assignment and send it to me before the start of class.
There's really no way to accept late work for the readings since it's vital that we're all reading the same papers at the same time.

All students are expected to follow the guidelines of the [UNC honor code](http://honor.unc.edu).
In the context of this class, it is particularly important that you cite the source of different ideas, facts, or methods and do not claim someone else's work as your own.
If you are unsure about which actions violate that honor code, or consult studentconduct.unc.edu.

## Conduct

I ask that we all follow the [NeurIPS Code of Conduct](https://nips.cc/public/CodeOfConduct) and the [Recurse Center Social Rules](https://www.recurse.com/social-rules).
Since this is a discussion class, it's especially important that we respect everyone's perspective and input.
In particular, I value the perspectives of individuals from all backgrounds reflecting the diversity of our students.
I broadly define diversity to include race, gender identity, national origin, ethnicity, religion, social class, age, sexual orientation, political background, and physical and learning ability.
I will strive to make this classroom an inclusive space for all students.
Please let me know if there is anything I can do to improve.

Acts of discrimination, harassment, interpersonal (relationship) violence, sexual violence, sexual exploitation, stalking, and related retaliation are prohibited at UNC-Chapel Hill.
If you have experienced these types of conduct, you are encouraged to report the incident and seek resources on campus or in the community.
Please contact the Director of Title IX Compliance/Title IX Coordinator (Adrienne Allison, adrienne.allison@unc.edu), Report and Response Coordinators (Ew Quimbaya-Winship, eqw@unc.edu; Rebecca Gibson, rmgibson@unc.edu; Kathryn Winn kmwinn@unc.edu), Counseling and Psychological Services (CAPs) (confidential) in Campus Health Services at (919) 966-3658, or the Gender Violence Services Coordinators (confidential) (Cassidy Johnson, cassidyjohnson@unc.edu; Holly Lovern, holly.lovern@unc.edu) to discuss your specific needs.
Additional resources are available at http://safe.unc.edu.

## Resources

The University of North Carolina at Chapel Hill facilitates the implementation of reasonable accommodations, including resources and services, for students with disabilities, chronic medical conditions, a temporary disability or pregnancy complications resulting in barriers to fully accessing University courses, programs and activities.

Accommodations are determined through the Office of Accessibility Resources and Service (ARS) for individuals with documented qualifying disabilities in accordance with applicable state and federal laws. See the ARS Website for contact information: https://ars.unc.edu or email ars@unc.edu.

UNC-Chapel Hill is strongly committed to addressing the mental health needs of a diverse student body. The Heels Care Network website (https://care.unc.edu) is a place to access the many mental resources at Carolina. CAPS is the primary mental health provider for students, offering timely access to consultation and connection to clinically appropriate services. Go to their website https://caps.unc.edu/ or visit their facilities on the third floor of the Campus Health building for an initial evaluation to learn more. 

Any student who is impacted by discrimination, harassment, interpersonal (relationship) violence, sexual violence, sexual exploitation, or stalking is encouraged to seek resources on campus or in the community. Reports can be made online to the EOC at https://eoc.unc.edu/report-an-incident/. Please contact the University’s Title IX Coordinator (Elizabeth Hall, interim – titleixcoordinator@unc.edu), Report and Response Coordinators in the Equal Opportunity and Compliance Office (reportandresponse@unc.edu), Counseling and Psychological Services (confidential), or the Gender Violence Services Coordinators (gvsc@unc.edu; confidential) to discuss your specific needs. Additional resources are available at safe.unc.edu.

## Changes

The professor reserves the right to make changes to the syllabus including project due dates and test dates. These changes will be announced as early as possible. 

