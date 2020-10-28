[![Build Status](https://travis-ci.com/suchow/test-manuscript.svg?branch=main)](https://travis-ci.com/suchow/test-manuscript)

# Understanding and Improving Human-bot Ecologies for Knowledge Generation

## Introduction

Knowledge generation happens online: Wikipedia articles are generated, 3D designs are shared, source code is forked and merged. Collectives are responsible for this generation. While collectives can be constituted entirely by humans, increasingly machines are part of the mix. For example, bots edit Wikipedia articles, generate 3D designs, and analyze source code. The machines are created by humans: Wikipedia editors create bots, platform owners create parametric model technologies, and developers create bots to enforce their own coding norms. Some of these environments have many machine agents; in Wikipedia there are over 1600 bots that contribute to articles at the same time as hundreds of thousands of editors. They don’t do the same thing as humans, but they are often built to assist human editors and take over tasks that can be easily automatable, like discovering broken URLs, or tasks that are not so easy to automate but should be done quickly, such as reverting edits that bring down the quality of articles. These collectives of humans and bots form an ecology, in the sense that the agents evolve over time, the agents interact with each other, and the agents interact with an environment, including the artifacts that they create, modify, and recombine.

Since knowledge generation is at the heart of the economy, our education systems, and our culture, understanding how these ecologies work is important. Moreover, these ecologies have the potential to shift and change in dramatic ways, because the technologies that underlie bots are changing radically, at a different rate than the human components are changing. This project will seek to better understand current human bot ecologies in order to help us anticipate and shape the future.

The time to do this research is now, because there have been significant changes in bots. Bots are sometimes seen as agents that interact closely with humans. For example, many bots used in industry are constructed as hybrid systems with humans in the loop [11, 33, 75]. At the same time, there are different kinds of large scale bots that are more or less autonomous. For example, much of the recent machine learning research based on transformer architectures [77] (GPT-3 [4], BERT [16], roBERTa , XLnet [88]) are framed around testing the ability of machines to train on large amounts of human generated content and then generate new content autonomously. These systems are increasing in capability but are not yet capable of generating human-level wikipedia articles, musical scores, or source code. While they are tested in bench marks in comparison to other systems and to humans, these systems are usually used by humans in a more interactive manner: parameters are tuned [28], prompts are changed, outputs are copyedited. They are at the very least tuned, as in the system CTRL. And most environments are not using these very large and complex systems: Wikipedia bots, for example, often operate more like a search and replace regular expression than like a context-aware text summarizer. More generally, both complex AI and much simpler automated knowledge generation systems can be used as tools with some degree of autonomy [68], at the service of a collection of humans. As tools get written, they are added to the mix. As in any ecology, when a new tool is added it may change the environment. They may eclipse their previous versions. Techniques may eclipse earlier techniques, effectively killing off some bots. It is also possible that some techniques might be used together, as a kind of ensemble. Experience with such mixed environments can inform future development.

This leads to a set of research questions: what happens when humans and bots interact together over time? What do humans build, and what do they use? To what degree do humans change in reaction to bot introductions? More generally, what learns: humans? Bots? Or some other kind of emergent structure?  These questions are answered in the context of knowledge generation. Answering them involves not just observing but also experimenting.  Each of the two years will involve observational studies, bench studies, and field studies.

Table 1. Summary of the research questions and activities to be undertaken
Y1: What is the design space of a human-bot ecology?
Y2: What emerges from human-bot ecologies?
1.1 Observational studies
2.1 Observational studies
1.2 Small group studies
2.2 Lab experiments: Bot explanations
1.3 Simulations
2.3 Simulations
1.4 Field studies
2.4 Field studies
1.5 Infrastructure building
2.5 Workshops and dissemination

## Expected intellectual merits
The intellectual merit of this work lies in a research plan that seeks to discover how interactions between agents and humans take place in settings where there are likely to be many human-human, human-machine, and machine-machine interactions, and where there is the possibility for the emergence of phenomena that have consequences for the creation of knowledge.

Our understanding of collaborative processes lags behind advances in computing to support these processes. The proposed work will contribute to the general understanding and design of processes that take advantage of the increasing capability of technologies in work settings. Augmenting humans with bots can potentially improve both teamwork and taskwork. To understand how work can be improved, the proposed research builds and tests theories using experiments. The project will thus advance theories and practice related to collectives that include human and machine components, and help model their reciprocal interactions. There is the potential to discover effective organizational forms that emerge from the interactions between machines and people.

## Expected broader impacts

Economic impact: The results of the proposed research may have a strong effect on the economy by increasing overall worker productivity, a result of using machines to augment human capabilities and provide better support for collaboration processes.

Infrastructure of Science: All models and source code developed by the investigators will be shared with the research community, and the models will be bundled and annotated for use in pedagogic settings. Data from the experiments, including transcripts of team interactions, will be shared as well.

Education and Training: The project will lead to technologies and processes that can be used directly to help teams of students or workers to perform collaborative tasks. These technologies and processes can be used as part of classroom and professional training in information systems, engineering, computer science, and interdisciplinary programs.

Broadening participation in STEM disciplines: The proposed work will also directly fund several students, including members of underrepresented groups. The investigators will run workshops for high school teachers and underrepresented minority high school students from Newark, NJ and surrounding communities who will participate in chatbot-augmented team science. Research suggests that the team-based approach to data science may help attract women into computing and engineering disciplines [30, 34, 67]. Synergistically, having women on teams increases team intelligence and facilitates more effective collaboration [54, 83].

## Rationale for a medium project
The project studies a complex and important phenomenon: how humans and bots can work together effectively to solve problems. To gain this understanding, we assembled a team able to apply a diversity of methods; the investigators have backgrounds in computer science, cognitive psychology, information systems, and organization science. Their research is housed in engineering, information, and management schools across four universities. Collectively the team has the combined skills to make progress along the social and technical dimensions of the problem in an integrated fashion. All the investigators have participated in large complex research projects and the Collaboration Plan discusses how the team will manage project risks and encourage research integration, drawing on the resources of an Industry Advisory Board. In sum, a Medium is warranted because there are large potential rewards for theories if we better understand how humans and bots do and should work together, and large potential rewards for the research community and society as a whole if the investigators are successful in building an open foundation of research tools and techniques that can be deployed to increase the productivity of teams.

## Theoretical background
In this study, we seek to understand how bots can improve collaboration in teams. Our study therefore draws on research related to chatbots and research related to teams, reviewed below.

### Ecologies

The concept of ecology has been applied to many domains: the term is used to describe the interactions between system components and the surrounding environment. Specifically, an ecosystem is "a system involving the interactions between a community of living organisms in a particular area and its nonliving environment” [10]. Ecosystems are dynamic and their processes are affected by external influences (like available energy or nutrients), internal factors (like the mix of species and the nature of the environment) and feedback loops. The components of biological ecosystems are linked by nutrient cycles and energy flows. Ecologies can be used to describe the energy inputs and outputs of organisms that interact with each other [5]. For example, plants consume sunlight, herbivores consume plants, and carnivores consume other animals. Food chains describe how the energy flows.

Outside of biology, the term has been generalized many times. Notably, human ecology is defined as the relationship between society and the environment [25]. Cognitive ecology has been defined in two ways: as the effects of decision making on animal fitness [70], and as the interrelationship of cognitive processes [26].

In the setting we seek to describe, what we call the human-bot ecosystem, we can be more specific. We define this ecology as "a system involving the interactions between a community of humans and computer agents running on a technological platform.” The platform serves as the environment and provides the infrastructure that enables, supports, and shapes the interactions among the participating humans and robots.


Both humans and robots in these systems can be equipped with different resources (knowledge, expertise, capability, information) and assume different roles. Their relationships can be interactive, adaptive, and co-evolving. Wikipedia is an example. Human editors and bots interact by editing / reverting one another’s work. They can adapt to one another by learning about the other party’s behaviors and altering their own behaviors or rules accordingly (e.g., bots learn about editor history and incorporate the information to better identify vandalism or humans learn from bot-initiated reversions to improve the quality of their edits). As a result, they co-evolve with one another and also with the environment, which in this case is the growing landscape of Wikipedia articles. One recent study described an ecology of bots [90]. The study showed how bots perform different functions, and how these functions were in some cases related to the functions human editors performed. What it didn’t address is the long-term dynamics of bots and people acting on each other.

One study discusses human-bot ecologies in relation to personal AI bots developed by a company called Luka. The study points out that bots are products that are distinct from the self, and their development provides the opportunity to create a less anthropomorphic culture [20]. By contrast, a paper focused on Wikipedia bots focuses on the practical implications of humans and bots working together to build data stores [66]. [what follows are attempts to motivate later studies by finding bridging ideas. Specifically, we will want constructs around attention and complexity I think.  It needs work...and references]

Ecologies in the natural world focus on how energy is transformed through food chains. In the case of the human bot ecologies being considered here, the scarce resource is attention. For human participants, this is where they focus their effort, and this effort is bounded by the hours in a day. For machines, effort relates to the use of CPU and memory. Machines can scale, but there are costs related to this scaling. As in an ecology, these two kinds of attention interact: for example, bad editing by a machine creates the need for humans to focus attention on fixing bad edits. Similarly, human vandalism leads to machines focusing resources on protecting rather than creating knowledge.

Ecologies also involve creating structures like dwellings that can be very complex. The effort of creating and maintaining a dwelling like a nest can trade off with other tasks such as looking for food. In the human bot ecology, the complexity of creating and maintaining a bot may divert attention away from other tasks, and so it is important to consider the advantages and drawbacks of complex vs simple bots, and, at a collective level, differences between sets simple bots vs sets of complex bots vs sets of bots of mixed complexity.

### Collaborative Writing and Software Writing Tools

There is a psychology to writing; writing is a kind of iterative problem solving that relies on motivation, perseverance, and learned skills [1, 15, 27, 43]. Writing by groups is common; indeed, in academic literature, an increasing number of papers are co-authored, sometimes by very large teams. Writing is a complex and consequential process, for individuals and for groups. Writing within it relies on complex skills such as planning. Technology can aid the writing process, but, at present moment, the vast majority of writing is done with a relatively simple technological assist through word processors which create persistence and allow fast revision. Because writing is a cognitively difficult process, it is a good one to study as a way of understanding computer supported cooperative work: it is unlikely that the task will fall entirely to computers, and it is not at all obvious which aspects of computationally enhanced writing, and which kinds of interfaces to software, will be most useful in the future.

The process of collaborative writing, and the effects of technology on the process, have been studied for decades in the CSCW community [2, 29, 50, 53, 55]. This work has highlighted the use of collaborative writing as a kind of interchange of many different forms of information, including process information, that eventually are edited out. Olson et al. noted that a kind of integrated writing environment might allow some of this information to persist in a kind of digital room [55]. Moreover, history might be used to recognize seismic types of events that had just happened or are about to happen (as when large chunks of text are about to be added). These analyses suggest there are many additional ways technology could enhance collaborative writing. However, the literature does not have a lot to say about the particular technologies that might be important for the next generation of tools. The earlier work took a role based approach, considering how authors work sometimes as reviewers with each other [2]. More recent work has opted for simpler, modeless tools [55]. While there are a number of different collaborative tools, these can be classified into two categories. The first are the synchronous tools, such as Google Doc or Etherpad, in which writers can simultaneously see their co-writers edits. The second are asynchronous tools, in which writers work on their own copies and merge them. Writing on Github is of this nature, as are tools such as ManuBot, which works on top of Github. Indeed, early studies of collaborative writing have noted different styles of writing, including synchronous group writing, parallel writing asynchronously, and turn taking [2].

In parallel, there have been many attempts to create software tools that aid individual writers. The Unix Writer’s workbench provided a large number of different tools that would analyze not just grammar but also many other aspects of writing, including readability, abstractness, and diversity,  [18, 19, 44]. Consistent with Unix toolsets, many different commands could be run, a kind of miscellany much like a usage or style guide provides - except automated.

At present time, commercial tools such as Grammarly have been studied with respect to how helpful they are in developing writing skills [56, 57]. The open source LanguageTool also provides grammar checking [47], and other open source projects continue [46].

More advanced tools are also on the horizon, including tools that automatically generate news stories [74]. These tools are immature, but are attracting attention in the journalism profession [17]. In the machine learning community, Natural Language Generation technologies have evolved in an intertwined way with natural language understanding technologies. One way to characterize the recent evolution of these technologies is through the perspective of context. While early NLP techniques were based on frames and other rule-based schemas, statistical techniques based on bags of words followed. These techniques were generalized to encompass context through embedding techniques that analyzed the order of words in large corpus. RNN and LSTM techniques looked at short sequences of words. Transformer techniques look at longer sequences of words, going back not just sentences but paragraphs. Attempts are being made to generalize these techniques for very large contexts - for example, books that might contain 100,000 words. At current writing, these transformer techniques are the subject of much research in both academia and industry: one of the largest trained models, GPT-3, is now part of a commercial service. Academics have been given access to these models to experiment with. But they are not yet part of everyday practice in most circumstances. That they might someday be part of everyday practice is possible. In particular, transformer-based technologies are being applied to the generation of customer service chatbots. While these technologies are advances, it is not yet clear how to harness them, and, indeed, how they are valuable in the context of human-based writing. For example, it may be that such tools are more valuable in writing commentary or summaries than writing the main text. Or it may be they are more valuable when combined with simple tools that scope their participation in the overall writing project.

## Overview of our approach and our evaluation plan

The project will involve a set of parallel activities. There is a component that involves observational work in analyzing the use of these technologies in place. There is another component that involves testing small parametric interventions. There are simulations, grounded in the human experiments, that seek to explore how emergence might take place. And there are longer running experiments to be run in which teams will use the technologies as part of collaborative writing projects. In the first year, there will be activities related to infrastructure building. In the second year, there will be dissemination activities, including high school related workshops and dissemination at conferences. The expectation is that the first year of activity most likely be practiced in a socially distant way, and that the second year can involve in person activities. If vaccines and other measures do not reduce the need for social distancing, the plan will still work; workshops and dissemination will happen online.
Year 0: Preliminary pilot research

In preparation for the proposal, the team engaged in prototype studies. With respect to observational studies, the group performed research on bots in Wikipedia environments, extending work published last year [90]. Figure 1 shows how a bot changes over time in relation to prototypical bots that perform specific roles.

Figure 1. This figure shows how the bot SuggestBot evolves over time in comparison to previously defined bot roles. The image was made using word embeddings to create a 2d space where each blue point is a different approved bot request for approval (BRFA) for SuggestBot. The arrows display the order in which the new BRFAs were approved.

Experiments were also performed. Specifically, investigator Suchow investigated two forms of infrastructure that might host experiments. The first is ManuBot, a  system that does writing based on Github. This system has a distinct advantage for this research: the system can take advantage of the current ecology of Github bots. It has the disadvantage that writers need to have some skill with using Github. Suchow also investigated Google Docs as a potential platform for bots. It is synchronous and easy to use. But it has a tight security model, making the deployment of hundreds of potential bots more complex. Both, though, are feasible environments for studies, and the proposal details how they will be used.

## Year 1: Delineating the design space of a human-bot ecology

The first year of the study will focus on understanding the design space of the human-bot ecology. The design space we define through a set of dimensions that correspond to choices that can be made with respect to the technologies and processes that host and govern a human bot ecology. The efforts of the first year will be to understand which dimensions in particular are the ones that have the most impact on outcomes of interest.
One outcome of interest is the quality of an artifact produced by human bot ecology. While we understand that, in traditional human environments, time on task correlates with quality, in a human bot environment, time can refer to both human attention and machine attention, the latter measured in CPU units. There may be different effects according to the ratio of these two kinds of attention. Moreover, machines may be aggregated into very large agents or broken into many smaller agents, and such decisions may influence how humans respond, and what phenomena emerge out of the interactions. These and similar issues will be pursued through a set of activities that use different methods.

For the experimental studies, we need environments and projects that involve collaborative knowledge generation work, and can be repeated relatively frequently. Writing papers, articles, and essays are all variants of the kind of knowledge work that are complex enough to exercise an ecosystem, but short enough in duration to allow for repeated experiment. Student writing is appealing in that teams can be configured and university subject pools can be used. Academic writing is appealing in that it utilized participants who are relatively expert at writing, and where complexity is high.

### 1.1 Observational studies

There are several well-established environments that can be viewed as human-bot ecologies. Not all of these environments are amenable to study: companies in many cases restrict the amount of data that academics can access. But several are, and these environments will be studied in order to better understand different aspects of human-bot ecology. What is learned from these studies will inform the experiments to be performed. And the experimental results may inform the observational studies: a simulation study may suggest something about modularity, and observation might then be directed to gather more data on, for example, changes in the modularity of particular ecologies. Three environments will be studied. The first is Wikipedia. Bots participate in editing articles together with human editors. The second is Github. Bots enforce norms within projects. Wikipedia is particularly open to being studied by academics: APIs make it possible to acquire consistent time series behavior on bots and edits. There are restrictions on understanding editors and their demographics, as well as individual viewer behavior. Github is a commercial product, but makes available an interface that allows for study of the environment. There are some restrictions on what can be seen, but in general it is possible to see bots and their actions. Moreover, most github bots have source code on github. Slack is a commercial product that has many more restrictions on the use of data than the other environments. But bot-building is relatively simple and widespread, and case studies can be performed on groups if they permit researchers to join their teams.

For each of these environments, the studies in year one will address the following research questions. A rough frame for these studies come from knowledge generation processes, which involve discovery, use, and invention. Humans need to discover tools. They then can attempt to use them; success at this may have to do with the quality of the interface and the complexity of the underlying bot. They may find problems with the tools and invent new ones. All of these are aspects of a human bot ecology. We don’t normally think of bots in the same way, but by analogy they do discover humans they can interact with, they do use the humans, by, for example, requesting they fix an edit, and they can potentially invent, if they are operating at a sufficient metalevel where they are learning and perhaps deploying improved versions of themselves.

### 1.1 Infrastructure Building Activities

#### 1.1.1 Bot building for human experiments
The main activity is building out a number of machine agents of various complexities that can be used in the experiments. We will leverage previous infrastructure built by investigator Suchow called proselint. The idea of proselint is that, much like a usage guide, a small set of simple bots can help improve writing by flagging or correcting problems or violations of norms in a text. In this case, proselint will be implemented on top of the ManuBot system.

#### 1.1.2 Simulation building for machine experiments

This work will involve building out an infrastructure that will allow for simulations with bot agents and simulated human agents, with the simulated human agent actions based on distributions from empirical data. Where human actions are important, crowd based approaches to simulation will be used; the investigators have used such approaches before.
The simulation platform will be based on…

#### 1.1.3 Educational demonstrations
Another component of this building educational demonstrations appropriate to use in workshops for high school teachers and students in year two.

## Activity 1.1: What bots are available for discovery in the context of collaborative writing.

This study has two parts. The first is classification task: typifying bots. We will use a technique that we have used to define the role of Wikipedia bots [90] and generalize it to other environments, in particular Github, whose bots have also been the subject of study [82]. Collaborative writing has also been studied on Github [42, 64, 65]. What is to our knowledge less studied is the conjunction of the two: how bots help in collaborative writing projects.

We will examine how bots are used in github writing projects, and what roles they play. We are interested in the extent to which their use is distinct from the use of bots in source code creation in github. And we are interested in how the use of Github Bots differs from the use of Wikipedia bots. In the case of Wikipedia, we have a way of evaluating the quality of the artifacts, the articles, from both the internal coding done by human editors and the automatic analysis done by the automated system ORES. With respect to team work, we will look at interaction patterns of teams, and the relationship between these patterns and the types bots used. Methodologically, we will start with simple techniques such as regression to identify interesting relationships, and augment these analyses with econometric techniques that can help establish causal relationships through the use of instrumental variables. There are aspects of these relationships that may exhibit network effects, and for those aspects we may utilize graph neural network techniques to see the extent to which past behaviors in the network can predict future behavior.

### Study 1.1.2

How are new bots invented?

This study will involve a combination of qualitative and quantitative approaches. It is possible to identify some of the creators of bots in these environments, and we will interview some of the creators to understand their experiences and their motivations. In particular, we will ask about the context in which they made decisions to build bots, and how they decided to modify their bots after release into production. This will be augmented by quantitative methods that will look at time series of bots, bot related documentation, and bot source code, to understand how the artifacts related to bot technology and governance change over time. Bots can be analyzed in detail in Github because the code and code changes are in github [31].  [more detail here on bot studies of github and/or wikipedia]

### Study 1.1.3
What happens when a bot is born (i.e., is introduced into the ecosystem)?
How do bots die (i.e., how are they removed from the ecosystem)?

In a biological ecology, there is birth and death. In this ecology, the analogical events are the entry of both bots and humans into the ecology, and their exit later. The introduction of humans has been studied in numerous newcomer studies. Less studied are the introduction of bots, and the interactions between bots and humans that may effect the overall environment. This study will use time series analysis to understand survival rates the factors that affect them.

### Study 1.1.4
How do bots coordinate with the users and each other? To what extent does the coordination happen stigmergically?

## 1.2 Bench Studies

Large human bot ecologies involve hundreds of thousands of human and machine participants. This makes repeated experiments challenging. One technique that can be used is to run small bench experiments that involve a limited number of humans and bots, with the goal of isolating factors that influence the outcomes of interest.  
One domain we understand and can control experimentally is collaborative writing. Arguably, both Wikipedia and Github are variants on collaborative writing, with Wikipedia focused mainly on articles and Github mainly on source code. Smaller versions of these environments can be built using wiki technology, or on top of other open source environments such as Etherpad or manubot, or utilizing commercial technology such as Google Docs. These environments allow  for bots to be written in a lightweight manner. One of the members of the team has implemented an open source application call proselint that can serve as the basis for a large set of agents that each perform a specialized writing related function (citation to https://github.com/amperser/proselint). This system will be further developed in activity 1.5. In particular, it will be implemented in the first year on top of ManuBot.
These studies require human participants. Since the tasks are writing tasks, we have several pools of people we can use to recruit participants. First, several of the universities participating are large; they have large formal subject pools, and, in addition, many students outside of subject pools who can be recruited. In addition, the investigators have experience with building crowd-based teams for experiments, and can utilize pools of participants from crowd work sites. Some of these sites have participants with strong copy editing skills, others with strong technology skills, so that experiments can be run across a skill gamut from novice to expert with respect to both writing and technology.

### 1.2.1 Discovery: How do humans discover bot capabilities? How do bots discover human capabilities?

In a small experimental setting, we can first observe how people discover capabilities, and how bots react to this discovery. We then can find ways of building processes that encourage discovery from both sides. In particular, we can assess the importance of bots building models of human capability.

### 1.2.2 Communication: How do and how should bots and humans communicate?
There are three dyadic pairing to consider: human human, human bot, and bot bot. Then there is collective communication, where bots or humans are flagging for all agents a task to be done. In the middle of a collaborative project with a mix of agents the communication will be in many cases mediated through the text being written. But it is possible for agents to write about the text, rather than writing text.
Just as human writers engage in meta-level discourse about an article, does metalevel-discourse help in situations where bots and humans are working together? For example, to what extent can meta-level comments from humans direct bots? To what extent can meta-level comments from bots help humans understand bot edits? To what extent can meta-level comments from bots help other bots understand if they can or should make more bot edits on top of bot edits?

While there is evidence from Wikipedia that meta-level information in the form of talk pages are useful for humans, and there is evidence that meta-level discourse in programming - for example decorators - can be useful to machines, it is unclear the extent to which meta-level comments will be helpful in an overall ecology, and, if helpful, exactly how to calibrate their use so as to not overshadow the creation of a main text.

In this study, bots will be built that have the capacity to both write and parse meta-level discourse, in particular comments about edits just made by the bot (justifications) and comments about passages that appear problematic (critique).

In the first set of experiments two such bots will be introduced into a setting with two humans. One bot will be focused on copy editing changes consistent with a style guide. Another will be focused on summarization, as in the creation of abstracts, paragraph initial and closing sentences, and section introductions. In initial experiments, a plan for a set of textual changes will be given to the human writers to implement. The writing task will be a wiki article, and ORES will be used to assess the quality of changes made after each edit. One dependent variable, then, will be the computational quality score from ORES. Human raters will also evaluate the edits. And the human writers will answer a set of questions about the effects of the bots on the article. The experiment will be run for at least 30 edits over a one week timeframe. The results will be used to calibrate the construction of bots for year two.

### 1.2.3 How does the complexity of bots change coordination?

At one one end of the spectrum are bots that simply rewrite strings based on lookups. At the other are transformer based systems trained on all available text. Interacting with one versus the other will affect not only one person, but potentially have larger effects. For example, complex bots may need more training, and may be trusted to generate longer pieces of text, that might eventually require downstream rewriting. In this study we create three conditions, one in which all bots are uniformly simple, another where the bot complexity is mixed, and a third where all bots are complex. [needs more on how we would do this and how long studies would run].

## 1.3 Simulations

While small studies can be used to examine some factors related to human bot ecology, factors related to scale need more participants. One way to explore issues of scale is through agent based modeling. In particular, agent based modeling is useful in modeling bot to bot interaction, as simulated bots can be made identical to bots used in production environments. Modeling human bot interaction is more challenging. However, given that the environment of collaborative writing is mediated through text, it is possible to use past human edit histories to calibrate human edit actions, providing a way to examine the possible effects of scale of both bots and humans interacting. In the first year, the simulation infrastructure will be built, and then calibrated based on the ongoing observational studies and experiments.


### 1.3.2
What is the carrying capacity of a human bot ecosystem?

There is a spectrum of mixes of humans and bots in an environment. At one extreme, there are hundreds of thousands of humans and hundreds of thousands of bots, the bots being specialized to perform particular actions or to help particular humans. At another extreme, large numbers of humans utilize one bot that has within it the capability of performing thousands of distinct interactions. This later architecture is akin to the way commercial bots such as Alexa and Siri function: they are constructed to appear like a unified human.

In these simulations we will explore issues related to discover and attention. These simulations will be calibrated by bench studies. The experiments on metalevel comments by bots will  provide enough of an empirical distribution of human and bot editing that a simulation could be run, with bots editing other bots comments, and a simulation injecting past human or human-like edits into the mix. Once instrumented, it will be possible to scale the number of bots and the number of humans to the point where the system reaches capacity, as manifest by decreasing quality of output or runaway text length or cyclic repetitive edits, a kind of thrashing.

### 1.3.3
What are the distinct ways to modularize these environments?
What combinations are theoretically possible?

New capabilities often come from combinations of modular components. Yet environments such as Wikipedia don’t consciously attempt to modularize bot and human behavior. What are the advantages and disadvantages of factoring human and machine processes and recombining them? For example, could bot functionality be factored in such a way that humans could readily recruit a small team that could work together to accomplish a task?

## 1.4 Field Studies

Another way to understand an ecology is to be embedded within it. In these studies, we plan to test human bot ecologies and record from within what happens.

### 1.4.1
What happens to a small team’s productivity as bots are introduced?

This study will look at what happens as technology is introduced. There will be a baseline period of collaboration on a writing project, followed by the introduction of a bot at various times in the cycle of writing. An initial study will be performed by the investigators who will use a system to write up the results of the year 0 and early year 1 studies. Subsequent studies will utilize student teams who will be given group writing assignments as part of their human subject participation credits. Eventually the system will be shared with other academics who will consent to the study of the traces of their collaborative work, and who will make themselves available for interviews at various stages of the project.

## Year 2: Encouraging the emergence of productive ecologies

The first year studies will have delineated the design space, and suggested what kinds of discovery, use, and invention may lead to productive ecologies. This second year looks to see if certain kinds of overall design encourages not only productive work, but the emergence of new practices and new tools. Infrastructure building and observational studies will continue, but the emphasis will be on lab and field studies.

### 2.1 Infrastructure building

#### 2.1.1. Bots
While the first year will have used an asynchronous form of collaborative editing based on Github, the second year will also compare an environment based on synchronous collaborative editing through Google docs

#### 2.1.2 Simulation
Simulations constructed in the first year can be better calibrated using the results of collected observational data as well as human subject experiments.

#### 2.1.3 Educational packaging
Portions of the infrastructure will be packaged so they can be used in high school workshops or undergraduate courses.

### 2.2 Observational studies

These studies will build on results of all the previous year’s studies. In particular, these will focus on understanding what emerges in large scale ecosystems, and how emergence happens.

#### 2.1.1.
How do humans discover emergent capabilities associated with multiple bots?
	How do humans discover emergent capabilities associated with human-bot ecosystems?
	What are the failure modes of human-bot ecosystems associated with a failure to
understand what’s possible?
Bots make mistakes. How do humans respond to bots’ mistakes?

####2.1.2
What roles emerge in a human-bot ecosystem?

#### 2.1.3
Are there interspecific transactive memory systems?

#### 2.1.4
How does learning take place in ecology?

This study looks at how human capabilities change over time, and how these relate to changes in machine capabilities. Is it the case that machines are adding capability more quickly than humans? If so, is this a result of the way the bots are being built, or a function of the increasing amount of training data available? The pragmatic result of this study may be an understanding of the kinds of human capabilities that can be trained going into an ecology and the kinds that can emerge as a result of interactions. The study might also help understand how machine learning capabilities can and should change in such environments.

### 2.3 Bench Studies

#### 2.3.1 Complex bots: Are transformers transformative?

While the first year will have looked at a mix of complexities, in this year one study will focus just on the use of complex text generating bots, the type that might be expected to generate sentences or paragraphs. These tools need prompts. And they need parameterization. We will seek to understand how these actually affect writing tasks. We plan to run 30 studies on small teams of students. We will supplement these studies with one longer study using academics who will use the tools as part of a project to produce an academic paper.

#### 2.3.2 Modularity: Bot chaining vs integrated bots

In an environment with many bots, one potential set of  ground rules is that bots don’t edit each other’s work. But an alternative set of ground rules would encourage this editing, in particular through the use of metacommunication that might direct bots to elaborate or fix passages just constructed by a different bot. It is not clear this would work: it might be that errors amplify. On the other hand, if it does work, it leads to the question of whether it would be better to integrate the various bots into one. Then it might be possible for the integrated bot to plan. But this integration might lose advantages of modularity. And it might lose the potential for human intervention through edits or through metacommunication to the bot.

#### 2.3.3 Communication and explainability

The ability of an author to explain a change may be important to the evolution of a text. Machine authors might also attempt to explain why they generate a change. This may help humans evaluate the change, and may also allow for metacommunication to the bot, maybe in natural language, maybe with a parameter. For example, if the bot says that it generated an abstract by summarizing the entire paper, a human might intervene and ask the bot to just summarize from the introduction and conclusion. These studies will try different types of explanation….

### 2.4 Simulations

Given the amount of data collected in the first year, the simulations can be calibrated better and rerun. New simulations will be created to better understand how attention can be directed in an ecosystem. In particular when does it make sense to build new technologies? New human processes? And when should technologies be decommissioned to create room for simpler or more effective technologies?

### 2.5 Field Studies

In these studies, we will make the bot infrastructure available to teams of scholars in our respective universities, and follow up on their usage by examining logs of changes to analyze behavior, and through interviews to elicit experiences about use and satisfaction.

## Results from Prior NSF Support
Jeffrey Nickerson (with John Nastasi): CHS: Small: Collective Design through Remixing; 14-22066; $499,150; August 2014 - July 2020. This research has focused on understanding and improving collective design. The focus of observational study has been an online open design community, Thingiverse. This past work is relevant because it analyzed the effects of an automated tool on collaboration.  Intellectual merit: Online communities encourage the collaborative exploration of design space, and this exploration can be measured objectively. This presents an opportunity for accomplishing collective-level design goals. An MISQ article [39], a JMIS article [80] and a Computers in Human Behavior article have been published [79], as have three chapters [48, 49, 76], one CSCW panel [51] and two CSCW papers [45, 89]. Sixteen papers have been published [22–24, 32, 36–38, 40, 50, 52, 59–63, 81], and one white paper [12]. A Communications of the ACM article and an IEEE Computer article on autonomous tools have been published [68, 69]. Broader impacts: The project has produced three PhDs [21, 35, 58], and included three MS students and two undergraduates, one an African American. The findings of this project have been incorporated into a product architecture curriculum. This work may increase participation in citizen engineering, and contribute to engineering for the long tail of unmet design needs.

Kevin Crowston: CHS Small: Supporting Stigmergic Coordination; 16-18444; Aug 2016 - Jul 2019; $499,931. The goal of this project is to first understand the socio-technical affordance enabling stigmergic coordination in free/libre open source software development teams (e.g., visibility of others’ work) and then to develop a system that provides similar affordances in a new domain, namely data-science teams. The first version of the system is currently being tested with two classes.  Intellectual merit: The initial work in this project has identified potential features that are important for enabling stigmergic coordination, such as systems like GitHub used for sharing source code and changes to source code, and work practices for how to make and share patches for bug fixing. The conceptual foundation for the study has been published as a journal article [3], a discussion of system affordances for stigmergy has been presented at a conference [13] and the theory and system have been described in a CSCW conference/journal paper [14]. Broader impacts: The project has involved a Ph.D. student and female postdoc, thus providing opportunities for training and education while broadening participation in science. The intent is to make the developed tools publicly available, which has the potential to improve the functioning of distributed teams and thus benefit society.

Yuqing Ren (with Robert E. Kraut, PI, Yan Chen & Qiaozhu Mei): IBSS-L: Developing, Testing, and Designing from a Computational Theory of Online Communities; 16-20319; Sep 2016 - Aug 2019; $919,979. Online communities have become commercially and societally important platforms butome do not last long enough to be effective while others do not achieve their production goals. We are building a computational theory of the factors and processes that make online communities successful. Intellectual merit: There have been few attempts to build a comprehensive, evidence-based theory to explain how online community attributes and processes interplay to determine community success. We address this gap by building and testing an integrated computational theory to predict community success at multiple levels of analysis, and then running field experiments. Nine papers have been published in journals and proceedings as a result of this work [6–9, 41, 84–87], and several more are in process. Broader impacts: Both the design guidelines and the agent-based model will have an important impact by improving the success of a wide variety of online communities and facilitating desirable outcomes such as crowd-sourced loans for online borrowers, psychological well-being of cancer patients in health support groups, and learning of students taking STEM courses, as well as outcomes in other online communities.

Walter Lasecki: SBIR Phase I: Exploring the Feasibility of Deployable Crowd-Powered Real-Time Captioning Supplemented with Automatic Speech Recognition, 1448616; $150,000; January 2015- December 2015. This project was an SBIR sponsored by a small business, Legion Labs in Pittsburgh, PA. Intellectual Merit: This award created a scalable web-based system called Scribe, which can be deployed in real classrooms to help deaf and hard of hearing students access spoken lectures. Broader Impacts: This system has been used in classrooms and academic conference venues, and enabled research on how crowd-generated captions can train automatic speech recognition systems on the fly to improve access.

Jordan Suchow (with Thomas L. Griffiths): The dynamics of updating and transmitting individual and collective memories, 1408652; Jul 2014 – Jun 2016; $172,425. Memory and culture form the foundation of human knowledge, which in turn drives scientific progress and technological advancement. Understanding the fundamental cognitive processes that shape memory and cultural transmission has traditionally fallen within the purview of psychologists and anthropologists. However, advances in statistics, machine learning, evolutionary dynamics, and network science offer a rich set of computational techniques for describing information transfer. Intellectual merit: Computational models were constructed that capture the cognitive dynamics of memory and culture, in order to understand the processes that shape them. A software platform was created for running experiments (see [78] for the GitHub), thereby enabling others to conduct their own experiments using these paradigms. The results were described at CogSci [73], the Crowdsourcing and Machine Learning Workshop at NuerIPS [72], and in the journal Trends in Cognitive Science [71]. Broader impacts: Better understanding the processes that affect maintenance of personal and collective memories reveals the conditions under which memories and cultural innovations are best maintained and possible techniques for improving them; this has broad economic and societal benefits.

## Conclusion
Collaborative systems that involve many people and machines are growing. These ecologies  may be useful for building knowledge. The proposed research will take a step in the quest to anticipate and shape the future of human bot ecologies.

## References

[1]	Alamargot, D. and Chanquoy, L. 2001. Through the Models of Writing: With Commentaries by Ronald T. Kellogg & John R. Hayes. Springer Science & Business Media.

[2]	Baecker, R.M., Nastos, D., Posner, I.R. and Mawby, K.L. 1995. The User-centred Iterative Design Of Collaborative Writing Software. Readings in Human–Computer Interaction. R.M. Baecker, J. Grudin, W.A.S. Buxton, and S. Greenberg, eds. Morgan Kaufmann. 775–782.

[3]	Bolici, F., Howison, J. and Crowston, K. 2016. Stigmergic coordination in FLOSS development teams: Integrating explicit and implicit mechanisms. Cognitive Systems Research. 38, Supplement C (Jun. 2016), 14–22.

[4]	Brown, T.B. et al. 2020. Language Models are Few-Shot Learners. arXiv [cs.CL].

[5]	Calow, P. 1987. Towards a Definition of Functional Ecology. Functional ecology. 1, 1 (1987), 57–61.

[6]	Chen, Y., Jiang, M., Kesten, O., Robin, S. and Zhu, M. 2018. Matching in the large: An experimental study. Games and economic behavior. 110, (Jul. 2018), 295–317.

[7]	Chen, Y., Lu, F. and Zhang, J. 2017. Social comparisons, status and driving behavior. Journal of public economics. 155, (Nov. 2017), 11–20.

[8]	Chen, Y., YeckehZaare, I. and Zhang, A.F. 2018. Real or bogus: Predicting susceptibility to phishing with economic experiments. PloS one. 13, 6 (Jun. 2018), e0198213.

[9]	Chen, Z., Lu, X., Ai, W., Li, H., Mei, Q. and Liu, X. 2018. Through a Gender Lens: Learning Usage Patterns of Emojis from Large-Scale Android Users. Proceedings of the 2018 World Wide Web Conference on World Wide Web (2018), 763–772.

[10]	Collins 1982. Collins English Dictionary. London & Glasgow.

[11]	Cranshaw, J., Elwany, E., Newman, T., Kocielnik, R., Yu, B., Soni, S., Teevan, J. and Monroy-Hernández, A. 2017. Calendar.Help: Designing a Workflow-Based Scheduling Agent with Humans in the Loop. Proceedings of the 2017 CHI Conference on Human Factors in Computing Systems (New York, NY, USA, 2017), 2382–2393.

[12]	Creamer, G.G., Ren, Y., Sakamoto, Y. and Nickerson, J.V. 2015. Ensembles of Crowds and Computers: Experiments in Forecasting. Stevens Institute of Technology School of Business Research Paper No. 2015–54.
[13]	Crowston, K., Østerlund, C.S., Howison, J. and Bolici, F. 2017. Work Features to Support Stigmergic Coordination in Distributed Teams. Academy of Management Annual Meeting (2017).

[14]	Crowston, K., Saltz, J., Rezgui, A., Hegde, Y. and You, S. 2019. Socio-technical affordances for stigmergic coordination implemented in MIDST, a tool for data-science teams. Proceedings of the ACM: Human-Computer Interaction. 3, CSCW (2019), Article 117.

[15]	Deane, P., Odendahl, N., Quinlan, T., Fowles, M., Welsh, C. and Bivens-Tatum, J. 2008. COGNITIVE MODELS OF WRITING: WRITING PROFICIENCY AS A COMPLEX INTEGRATED SKILL. ETS Research Report Series. 2008, 2 (Dec. 2008), i–36.

[16]	Devlin, J., Chang, M.-W., Lee, K. and Toutanova, K. 2018. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. arXiv
[cs.CL].

[17]	Diakopoulos, N. 2019. Automating the News: How Algorithms Are Rewriting the Media. Harvard University Press.

[18]	Frase, L.T. 1983. Human factors and behavioral science: The UNIXTM Writer’S workbench software: Philosophy. The Bell System Technical Journal. 62, 6 (Jul. 1983), 1883–1890.

[19]	Gingrich, P.S. 1983. Human factors and behavioral science: The UNIXTM Writer’s Workbench software: Results of a field study. The Bell System Technical Journal. 62, 6 (Jul. 1983), 1909–1921.

[20]	Guilbeault, D. and Finkelstein, J. 2018. Human–Bot Ecologies. A networked self and human augmentics. (2018).

[21]	Han, Y. 2017. Collective Exploration: Understanding Remixing Patterns in Online Communities. Ph.D. Dissertation, Stevens Institute of Technology.

[22]	Han, Y. and Nickerson, J.V. 2015. Exploring Design Space Through Remixing. Collective Intelligence (2015).

[23]	Han, Y. and Nickerson, J.V. 2017. The Generativity of Remixing: Understanding Knowledge Reuse Process for Innovation in Online Communities. Proceedings of the International Conference on Information Systems (2017).

[24]	Han, Y. and Nickerson, J.V. 2015. Understanding the Exploration of Design Space in Remix Networks. Workshop on Information in Networks (2015).

[25]	Hawley, A.H. 1986. Human Ecology: A Theoretical Essay. University of Chicago Press.

[26]	Hutchins, E. 2010. Cognitive ecology. Topics in cognitive science. 2, 4 (Oct. 2010), 705–715.

[27]	Kellogg, R.T. 1999. The Psychology of Writing. Oxford University Press.

[28]	Keskar, N.S., McCann, B., Varshney, L.R., Xiong, C. and Socher, R. 2019. CTRL: A Conditional Transformer Language Model for Controllable Generation. arXiv [cs.CL].

[29]	Kim, J., Sterman, S., Cohen, A.A.B. and Bernstein, M.S. 2017. Mechanical Novel: Crowdsourcing Complex Work through Reflection and Revision. Proceedings of the 2017 ACM Conference on Computer Supported Cooperative Work and Social Computing (New York, NY, USA, Feb. 2017), 233–245.

[30]	Knight, D.W., Carlson, L.E. and Sullivan, J.F. 2003. Staying in engineering: Impact of a hands-on, team-based, first-year projects course on student retention. Proceedings of the ASEE Conference (2003).

[31]	Kollanyi, B. 2016. Automation, Algorithms, and Politics| Where Do Bots Come From? An Analysis of Bot Codes Shared on GitHub. International Journal of Communication Systems. 10, 0 (Oct. 2016), 20.

[32]	Kruse, L.C. and Nickerson, J.V. 2018. Portraying Design Essence. HICSS (2018).

[33]	Kucherbaev, P., Bozzon, A. and Houben, G. 2018. Human-Aided Bots. IEEE Internet Computing. 22, 6 (Nov. 2018), 36–43.

[34]	Kuhn, P. and Villeval, M.C. 2015. Are Women More Attracted to Co-operation Than Men? The Economic Journal. 125, 582 (2015), 115–140.

[35]	Kyriakou, H. 2016. Collective innovation: Novelty, reuse and their interplay. Ph.D. Dissertation, Stevens Institute of Technology.

[36]	Kyriakou, H. and Nickerson, J.V. 2015. Novelty and Reuse in an Open Innovation Community. Workshop on Information in Networks (WIN), New York University, New York, NY (2015).

[37]	Kyriakou, H. and Nickerson, J.V. 2016. Twitch Plays Pokémon: An Exploratory Analysis of Mass Synchronous Crowd Collaboration. Collective Intelligence (2016).

[38]	Kyriakou, H., Nickerson, J. V., Majchrzak, A. 2017. Makers of the Artificial: What Strategies Lead to Design Reuse? WITS (2017).

[39]	Kyriakou, H., Nickerson, J.V. and Sabnis, G. 2017. Knowledge Reuse for Customization: Metamodels in an Open Design Community for 3D Printing. MIS Quarterly. 41, 1 (2017), 315–332.

[40]	Lindberg, A. and Nickerson, J.V. 2016. Sequential Innovation Patterns: Online Experiments on Creative Processes. Collective Intelligence (2016).

[41]	Liu, T.X., Bednar, J., Chen, Y. and Page, S. 2018. Directional behavioral spillover and cognitive load effects in multiple repeated games. Experimental Economics. (Apr. 2018), 1–30.

[42]	Longo, J. and Kelley, T.M. 2015. Use of GitHub as a platform for open collaboration on text documents. Proceedings of the 11th International Symposium on Open Collaboration (New York, NY, USA, Aug. 2015), 1–2.

[43]	MacArthur, C.A. and Graham, S. 2016. Writing research from a cognitive perspective. Handbook of writing research., 2nd ed. 2, (2016), 24–40.

[44]	Macdonald, N.H. 1983. Human factors and behavioral science: The UNIXTM Writer’s Workbench software: Rationale and design. Bell System Technical Journal. 62, 6 (1983), 1891–1908.

[45]	Malone, T.W., Nickerson, J.V., Laubacher, R.J., Fisher, L.H., De Boer, P., Han, Y. and Towne, B. 2017. Putting the Pieces Back Together Again: Contest Webs for Large-Scale Problem Solving. Computer-Supported Cooperative Work & Social Computing (2017).

[46]	Miłkowski, M. 2010. Developing an open-source, rule-based proofreading tool. Software: practice & experience. 40, 7 (2010), 543–566.

[47]	Naber, D. and Others 2003. A rule-based style and grammar checker. (2003).

[48]	Nickerson, J.V. 2015. Collective design: remixing and visibility. Design Computing and Cognition’14. Springer. 263–276.

[49]	Nickerson, J.V. 2017. Diagrams in Design. Psychological Representations in Mind and World. J.M. Zacks and H.A. Taylor, eds. Psychology Press., New York, NY.

[50]	Nickerson, J.V., Han, Y. and Ozturk, P. 2017. Collaborative Editing as Collective Creativity. Fifteenth International Workshop on Collaborative Editing Systems at CSCW (2017).

[51]	Nickerson, J.V., Malone, T.W., Olson, G.M. and Crowston, K. 2015. Collective Problem Solving: Features and affordances of creative online communities. Proceedings of the 18th ACM Conference Companion on Computer Supported Cooperative Work & Social Computing (2015), 135–138.

[52]	Nickerson, J. V., Zheng, L., Bouwense, C., Mai, F., and Gordon, D. M. 2018. Implicit Coordination in Peer Production Networks. Collective Intelligence (2018).

[53]	Noël, S. and Robert, J.-M. 2004. Empirical Study on Collaborative Writing: What Do Co-authors Do, Use, and Like? Computer supported cooperative work: CSCW: an international journal. 13, 1 (Mar. 2004), 63–89.

[54]	OECD 2017. PISA 2015 Results (Volume V) Collaborative Problem Solving. (Nov. 2017). DOI:https://doi.org/10.1787/9789264285521-en.

[55]	Olson, J.S., Wang, D., Olson, G.M. and Zhang, J. 2017. How People Write Together Now: Beginning the Investigation with Advanced Undergraduates in a Project Course. ACM Trans. Comput.-Hum. Interact. 24, 1 (Mar. 2017), 1–40.

[56]	ONeill, R. and Russell, A. 2019. Stop! Grammar time: University students’ perceptions of the automated feedback program Grammarly. Australasian Journal of Educational Technology. 35, 1 (2019).

[57]	O’Neill, R. and Russell, A.M.T. 2019. Grammarly: Help or hindrance? Academic Learning Advisors’ perceptions of an online grammar checker. Journal of Academic Language and Learning. 13, 1 (2019), A88–A107.

[58]	Ozturk, P. 2017. Dynamics of Online Community Collaborations. Ph.D. Dissertation, Stevens Institute of Technology.

[59]	Ozturk, P., Han, Y., Towne, W.B. and Nickerson, J.V. 2016. Topic Prevalence and Reuse in an Open Innovation Community. Collective Intelligence (2016).

[60]	Ozturk, P. and Nickerson, J. 2015. Paths from Talk to Action. Proceedings of the International Conference on Information Systems (2015).

[61]	Ozturk, P. and Nickerson, J.V. 2017. Dialog classification in Wikipedia. Collective Intelligence (2017).

[62]	Ozturk, P. and Nickerson, J.V. 2015. Modularity and Productivity in WikiProjects. Workshop on Information in Networks (2015).

[63]	Ozturk, P. and Nickerson, J.V. 2015. WikiProjects: Collaborative Product Development Teams. Collective Intelligence (2015).

[64]	Pe-Than, E.P.P., Dabbish, L. and Herbsleb, J.D. 2019. Collaborative Writing at Scale: A Case Study of Two Open-Text Projects Done on GitHub. (2019).

[65]	Pe-Than, E.P.P., Dabbish, L. and Herbsleb, J.D. 2018. Collaborative Writing on GitHub: A Case Study of a Book Project. Companion of the 2018 ACM Conference on Computer Supported Cooperative Work and Social Computing (New York, NY, USA, Oct. 2018), 305–308.

[66]	Piscopo, A. 2018. Wikidata: A New Paradigm of Human-Bot Collaboration? arXiv
[cs.HC].

[67]	Rhoten, D. and Pfirman, S. 2007. Women in interdisciplinary science: Exploring preferences and consequences. Research policy. 36, 1 (Feb. 2007), 56–75.

[68]	Seidel, S., Berente, N., Lindberg, A., Lyytinen, K. and Nickerson, J.V. 2019. Autonomous Tools and Design: A Triple-loop Approach to Human-machine Learning. Communications of the ACM. 62, 1 (2019), 50–57.

[69]	Seidel, S., Berente, N., Marinez, B., Lindberg, A., Lyytinen, K., Nickerson, J.V. 2018. Autonomous Tools in Systems Design: Reflective Practice & Ubisoft’s Ghost Recon Wildlands Project. IEEE Computer. (2018), 16–23.

[70]	Stamp Dawkins, M. 1998. Cognitive ecology: the evolutionary ecology of information processing and decision making. Trends in cognitive sciences. 2, 8 (Aug. 1998), 304.

[71]	Suchow, J.W., Bourgin, D.D. and Griffiths, T.L. 2017. Evolution in Mind: Evolutionary Dynamics, Cognitive Processes, and Bayesian Inference. Trends in Cognitive Sciences. 21, 7 (Jul. 2017), 522–530.

[72]	Suchow, J.W. and Griffiths, T.L. 2016. Rethinking experiment design as algorithm design. Crowdsourcing and Machine Learning Workshop at NIPS (2016).

[73]	Suchow, J.W., Pacer, M.D. and Griffiths, T.L. 2016. Design from zeroth principles. Proceedings of the 38th Annual Conference of the Cognitive Science Society (2016).

[74]	Thurman, N., Dörr, K. and Kunert, J. 2017. When reporters get hands-on with robo-writing: Professionals consider automated journalism’s capabilities and consequences. Digital journalism. 5, 10 (2017), 1240–1259.

[75]	Toxtli, C., Monroy-Hernandez, A. and Cranshaw, J. 2018. Understanding Chatbot-mediated Task Management. Proceedings of the 2018 CHI Conference on Human Factors in Computing Systems (New York, NY, USA, 2018), 58:1–58:6.

[76]	Tversky, B., Gao, J., Corter, J.E., Tanaka, Y. and Nickerson, J.V. 2016. People, place, and time: inferences from diagrams. International Conference on Theory and Application of Diagrams (2016), 258–264.

[77]	Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A.N., Kaiser, Ł.U. and Polosukhin, I. 2017. Attention is All you Need. Advances in Neural Information Processing Systems 30. I. Guyon, U.V. Luxburg, S. Bengio, H. Wallach, R. Fergus, S. Vishwanathan, and R. Garnett, eds. Curran Associates, Inc. 5998–6008.

[78]	Wallace Github Repository: http://github.com/berkeley-cocosci/Wallace. Accessed: 2018-05-30.

[79]	Wang, K. and Nickerson, J.V. 2017. A literature review on individual creativity support systems. Computers in Human Behavior. 74, (2017), 139–151.

[80]	Wang, K. and Nickerson, J.V. 2019. Wikipedia-based method to support creative idea generation: The Role of Stimulus Relatedness. Journal of Management Information Systems. 36, 4 (2019), 1–29.

[81]	Wang, K., Nickerson, J.V. and Sakamoto, Y. 2018. Crowdsourced Idea Generation: The Effect of Exposure to an Original Idea. Creativity and Innovation Management. 27, 2 (2018), 196–208.

[82]	Wessel, M., de Souza, B.M., Steinmacher, I., Wiese, I.S., Polato, I., Chaves, A.P. and Gerosa, M.A. 2018. The Power of Bots: Characterizing and Understanding Bots in OSS Projects. Proc. ACM Hum.-Comput. Interact. 2, CSCW (Nov. 2018), 1–19.

[83]	Woolley, A.W., Chabris, C.F., Pentland, A., Hashmi, N. and Malone, T.W. 2010. Evidence for a collective intelligence factor in the performance of human groups. Science. 330, 6004 (2010), 686–688.

[84]	Yang, D., Halfaker, A., Kraut, R. and Hovy, E. 2016. Edit categories and editor role identification in Wikipedia. Proceedings of the Tenth International Conference on Language Resources and Evaluation (LREC 2016) (2016), 1295–1299.

[85]	Yang, D., Halfaker, A., Kraut, R. and Hovy, E. 2017. Identifying semantic edit intentions from revisions in wikipedia. Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing (2017), 2000–2010.

[86]	Yang, D., Halfaker, A., Kraut, R. and Hovy, E. 2016. Who did what: Editor role identification in Wikipedia. Tenth International AAAI Conference on Web and Social Media (2016).

[87]	Yang, D. and Kraut, R.E. 2017. Persuading Teammates to Give: Systematic Versus Heuristic Cues for Soliciting Loans. Proc. ACM Hum. -Comput. Interact. 1, CSCW (Dec. 2017), 114:1–114:21.

[88]	Yang, Z., Dai, Z., Yang, Y., Carbonell, J., Salakhutdinov, R.R. and Le, Q.V. 2019. XLNet: Generalized Autoregressive Pretraining for Language Understanding. Advances in Neural Information Processing Systems 32. H. Wallach, H. Larochelle, A. Beygelzimer, F. d\textquotesingle Alché-Buc, E. Fox, and R. Garnett, eds. Curran Associates, Inc. 5753–5763.

[89]	Zheng, L.N., Albano, C.M., Vora, N., Mai, F. and Nickerson, J.V. 2019. The Role Bots Play in Wikipedia. Proceedings of the ACM: Human-Computer Interaction. 3, CSCW (2019). DOI:https://doi.org/10.1145/3359317.

[90]	Zheng, L. N., Mai, F., Albano, C. M., Vora, N. and Nickerson, J. V. 2019. The Role Bots Play in Wikipedia. Proceedings of the ACM: Human-Computer Interaction. 3, CSCW (2019).
