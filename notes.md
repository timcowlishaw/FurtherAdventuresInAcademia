# My finkings on masheen lerning

## Topics to cover
  - Related challenges
     - Information retrieval
     - Topic extraction (and ontology relationship detection)
     - Named entity recognition
     - Word-sense disambiguation
     - Feature selection for active learning.

  - Lines of enquiry
    - Suitable models
    - Suitable query strategies and error / uncertainty measures
    - Methods of incorporating outside knowledge
    - Feature selection for AL on broadcast archives
    - Methods of incorporating visual / audible features, or feeding back into transcription process
    - Application to statistical relational learning
    - Modelling individual users as drawn from a topic distribution
    - Use of active learning to overcome HCI challenges related to machine learning for IR
    - Evaluation of existing algorithms and models in broadcast archive setting.
    - Improvement of existing results by incorporating structured background knowledge
    - Investigation of Human Computer Interaction and IR challenges related to active learning


## Notes from chat with Nicolas @ detective.io

 - Precision / recall tradeoff is hard for journalism! Depends on context / needs.
 - detective.io entirely manual classification / entry
 - user-defined ontologies very useful
 - Focused more on long-term, open ended investigation than highly time-sensitive 'breaking news' stuff.
 - Talk to [Hille van der Kaa](http://hillevanderkaa.wix.com/deuitgeeffabriek#!english/c6rz) at [University of Tilberg](http://www.tilburguniversity.edu/education/masters-programmes/data-journalism/).
 - UI frustrations with existing ML tools like [PULS](http://puls.cs.helsinki.fi/) - not solving the right problem.
 - Mentioned [Overview](http://overview.ap.org/) - tool used for discovery within large text corpora.
 - Problems with big general-purpose datasets eg FiveThirtEight on [Nigerian Kidnappings](http://fivethirtyeight.com/datalab/nigeria-kidnapping/) and use of [GDELT](http://gdeltproject.org/), see [here](https://storify.com/AABoyles/how-to-gdelt-properly?utm_source=t.co&utm_content=storify-pingback&utm_campaign=&awesm=sfy.co_qVYB&utm_medium=sfy.co-twitter) and [here](https://source.opennews.org/en-US/articles/gdelt-decontextualized-data/).

## Email to James @ Guardian
  Hi there James,

Thanks very much for passing your details on! I'm currently working on a PhD proposal, which, if all goes to plan, I'm hoping to begin researching in September. My proposed thesis title is "Active learning for semantic annotation of large media archives, in the presence of structured background knowledge", and I have some tentative ideas about how my research might prove useful for journalists, on which I'd love to hear your thoughts!

Being as brief as I can, my proposal outlines a novel approach to the categorisation of large archives of textual information, and the annotation of it with semantic metadata (think topics, locations, people and events mentioned or described). Common supervised machine learning approaches to this problem require a 'training set' of information, manually annotated with ground-truth labels on which to train a model. However, in many cases, it can be incredibly costly to produce such a training set - given that a subject expert, archivist or researcher must manually label a (normally large) number of training examples.

Active learning (also known as query learning) offers an alternative approach to supervised classification problems such as this - instead of requiring a large pre-annotated training set, an active algorithm is trained from an un-annotated set of examples, and interactively queries a human operator for ground-truth labels on those examples it judges to be most significant to the model. Existing empirical results suggest that active algorithms offer an improvement over traditional 'batch' supervised learning in terms of the number of labelled examples needed to reach a given level of predictive accuracy, in many contexts.

I'm proposing to study the use of active learning to solve information retrieval problems in broadcasting - specifically by applying techniques from active learning to the problems faced by researchers and journalists using the BBC's archive of broadcasted video and audio. (I've worked with the BBC professionally on this system and am hoping to spin my work out into a topic for research!). Basically, the BBC has a very large online archive of all broadcasted material, which is used by researchers internally to find existing media which is relevant to some area of interest, such as the subject of a new documentary programme. however, while we have text transcriptions of most of the archive, which facilitates searching by terms mentioned in a programme, there is only very sparse coverage of semantic metadata related to programmes - specific people featured, locations depicted, events or topics mentioned, or time-frames covered.

This sort of metadata is invaluable for discovery purposes, as, combined with knowledge about the relationships between the entities described by the metadata, it admits both improved recall when searching for specific topics (a search for "First World War", should include results mentioning "Passchendaele",even if the phrase "First World War" is not explicitly mentioned), and richer means of navigating through the archive (For instance, navigating from programmes about the First World War to programmes about events which occurred concurrently with it, or drilling down into programmes about specific events like "Armistice day", or people, such as "Gavrilo Princip").
