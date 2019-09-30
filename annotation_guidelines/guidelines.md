# Annotation guidelines for NoReC_eval
January 2019

# Table of Contents

1. [Introduction](#introduction)
2. [Evaluative sentences](#evaluative-sentences)\
2.2 [Mixed sentiment](#mixed-sentiment)\
2.3 [Explicit and implicit sentiment](#explicit-and-implicit-sentiment)\
2.4 [About the annotation process](#about-the-annotation-process)
3. [WebAnno](#webanno)\
3.2 [Marking sentences](#marking-sentences)\
3.3 [Change how many sentences are visible](#change-how-many-sentences-are-visible)\
3.4 [Change font size](#change-font-size)\
3.5 [Change password](#change-password)
4. [Part 1: Labels and attributes](#part-1-labels-and-attributes)\
4.2 [Aspect](#aspect)\
4.3 [Label: Evaluation](#label-evaluation)\
4.4 [Attribute: First-person](#attribute-first-person)\
4.5 [Attribute: Topic relevance](#attribute-topic-relevance)\
4.6 [Attribute: Disagreement](#attribute-disagreement)\
4.7 [Overlap](#overlap)
5. [Part 2: Identifying the correct labels](#part-2-identifying-the-correct-labels)\
5.2 [Sentence Types](#sentence-types)\
5.3 [Less Challenging Sentences](#less-challenging-sentences)\
5.3.1 [Emotional Sentences](#emotional-sentences)\
5.3.2 [Rational evaluations with sentiment lexemes](#rational-evaluations-with-sentiment-lexemes)\
5.3.3 [Other Gradable and Relational Adjectives](#other-gradable-and-relational-adjectives)\
5.4 [Evaluative Fact-Implied Non-Personal Sentences](#evaluative-fact-implied-non-personal-sentences)\
5.5 [Subjective, but not Evaluative](#subjective-but-not-evaluative)\
5.6 [Modifiers](#modifiers)\
5.7 [Label Guide Summary](#label-guide-summary)\
5.8 [Problems](#problems)
6. [Special Cases](#special-cases)\
6.2 [Sarcasm and Irony](#sarcasm-and-irony)\
6.3 [Exclamations and Imperatives](#exclamations-and-imperatives)\
6.4 [Modality](#modality)\
6.4.1 [Kunne (can, could)](#kunne-cancould)\
6.4.2 [Burde (should)](#burde-should)\
6.5 [Irrealis](#irrealis)\
6.6 [Questions](#questions)\
6.7 [Comparative Sentences](#comparative-sentences)\
6.8 [Difficult Lexemes](#difficult-lexemes)
7. [Summary and Tips](#summary-and-tips)\
7.2 [Test](#test)\
7.3 [Test: suggested labels](#suggested-labels)


## Introduction
Sentiment Analysis is often approached by first locating the relevant, sentiment-bearing sentences.
Traditionally, one has distinguished between subjective and objective sentences, where only the former were linked to sentiment. Objective sentences typically present facts about the world, whereas subjective sentences express personal feelings, views, or beliefs. 
This relation between sentiment and subjectivity has been problematized by, among others, Liu (2012, sec 2.4, ch. 4, [link](https://www.cs.uic.edu/~liub/FBS/SentimentAnalysis-and-OpinionMining.pdf)) who argues that one may find subjective sentences that do not express sentiment, e.g. *I think that he went home*, as well as objective sentences that do, e.g. *The earphone broke in two days*.

## Evaluative sentences
In this annotation effort, we will therefore focus on locating **evaluative** (opinionated) sentences in Norwegian reviews. These reviews are taken from the Norwegian Review Corpus ([NoReC](https://github.com/ltgoslo/norec), 2018). We define an evaluative sentence as a sentence that expresses or implies a positive or negative evaluation, regardless of its subjectivity. This means that only the sentence *The earphone broke in two days* discussed above is evaluative, since it expresses a negative sentiment about the earphone. Note that these terms are used somewhat differently in the literature.


<!--- burde det stå noe om "opinion"? --->

### Mixed sentiment
We distinguish evaluative from non-evaluative sentences, however, we do not mark their sentiment as positive or negative directly. One reason for this is that it is not always straight-forward to determine sentiment on the sentence level. One sentence may, in fact, express both positive and negative sentiment, e.g. *The screen is large but the battery capacity is weak*. 

### Explicit and implicit sentiment
We do not require the presence of an explicit sentiment-bearing expression for the recognition of a sentence as evaluative. This means that both a sentence with an explicit sentiment-bearing expression, e.g. *I love this phone* and a sentence which only implicitly expresses a sentiment *There is a pool* (in a hotel review) should be considered to be opinionated. However, we do mark both types of evaluative sentences differently in the sentence leval annotation, in order to differenciate between them.

### About the annotation process
Like some other previous attempts, we will attempt a two-staged annotation process (see [Toprak et al.](https://www.aclweb.org/anthology/P/P10/P10-1059.pdf), 2010 ) The first stage is the sentence level annotation stage. The second stage is based on the sentences extracted from the first round, and is more fine grained. So far, these annotation guidelines only comprise the first (sentence) level of the annotation process.

First, a short introduction to the annotation tool WebAnno is given. Then, part 1 explains the terminology and labels needed for the annotation, while part 2 explains the annotation process, related problems and gives examples for all of these.

<!--- denne burde kanskje oppdateres så den stemmer mer overens med innholdsfortegnelsen?--->

Example sentences are identified by their NoReC ID (6 digits) and the sentence number and their labels are indicated after the ID, like in the following example:

    Variert og spennende [601625:1] (E)

## WebAnno
WebAnno is a free-to-use web annotation tool. For the full user guide see the [WebAnno user guide](https://webanno.github.io/webanno/releases/2.3.0/docs/user-guide.html). Following is a short introduction to the most necessary functions for the annotators.

### Starting and finishing a document

When you log in, you will see a button called annotation. Click this to get an overview of available projects. Under each project, you can select a document to annotate. When you have completely finished annotating, and when you are pleased with your annotation, you can click the finish icon in the right corner. Your annotation will then be sent to the curator for further profcessing, and you will not be able to make any changes to it.

### Marking sentences

Annotation in WebAnno is done in so-called *layers*. These layers indicate which syntactic level the annotation is done at, such as word level, phrase level, or as in our case, sentence level. The layer “Sentence level SA" is already marked when you start your annotation. To mark a sentence, double click or mark parts of the sentence with the cursor. For the time being there are no shortcut keys for marking sentences that we are aware of.

When a sentence is marked, the annotator can select one label and three attributes. Annotators should only worry about the first two attributes: topic relevance and first-person. Sentences must have one of the three evaluative labels before they can be given any of the remaining attributes. The last attribute, *disagreement*, is only used by the curator/admin. The labels can be toggled using the TAB key and the arrow keys, allowing for quicker (and more comfortable) labeling.

If you want to change the labels you have chosen for a sentence, double left click on the **labels**, not the sentence itself, doing so will reset the sentence.

[image2]: https://github.com/ltgoslo/norec_eval/blob/master/annotation_guidelines/labels2.png "Labels"

![alt text][image2]
*Image 1: A labeled sentence*

See part 1 and 2 for details surrounding the actual annotation rules.

### Change how many sentences are visible. 
You can change how many sentences that are visible on one page by clicking settings -> visible sentences and then selecting the appropriate number. Note that if you have selected a number lower than the number of sentences, you might still experience that some of the sentences “disappear”. They should show up when you start marking sentences that are close to them.

[image1]: https://github.com/ltgoslo/norec_eval/blob/master/annotation_guidelines/visible_sentences.png "Visible sentences"

![alt text][image1]
*Image 2: Changing the visible sentences parameter*

### Change font size
You can also change the font size in **settings**, where it is called *font zoom*.

### Change password
Contact the administrator to change your password.

# Part 1: Labels and attributes

Each sentence must be labeled with one evaluative label, or remain completely unlabeled. In addition to an evaluative label, a sentence can be given an attribute from either topic relevance or first-person. In our experience, deciding topic relevance or first-person does not pose much difficulty, while evaluation can be tricky. Sentences are only labeled as not-on-topic or non-first-person if they are assigned one of the evaluative labels. An evaluative sentence which has not been labeled as not-on-topic or non-first-person is to be understood as first-person and on-topic. 

### Aspect
In the discussion of labels and attributes some terminology taken from more detailed analyses is necessary. One of these is the term _aspect_. This term is used to mean some part or aspect of the object being reviewed. For example, a movie can have several aspects: screenplay, actor performance, quality, length, etc. A camera can have aspects such as battery time, price, resolution, weight, etc. On the other hand, the theme and genre of a movie is not necessarily on topic. A comment about romantic movies in general does not necessarily include an evaluation of the movie being reviewed. Note, however, that if an evaluation is about a group that subsumes the object being reviwed, we consider the evaluation on topic. This means that in a review about the novel _Harry Potter and the Philosopher's stone_, a sentence like "I love all of JK Rowling's books" should be considered an evaluative sentence.

### Label: Evaluation
A sentence must be labeled as either just evaluative (E) or as the subclass evaluative fact-implied non-personal (E-FINP). Deciding whether a sentence is purely evaluative, evaluative fact-implied non-personal or neither of these can be more problematic, but trust your judgement, and take a note of sentences you find difficult, so that they can be discussed by all annotators.

### Attribute: First-person
We make a distinction between first-person and non-first-person sentences. As with the topic attribute, sentences are only explicitly given the attribute non-first-person (NFP) if they are assigned one of the evaluative labels. A sentence is first person if the holder of the evaluation corresponds to the author(s) of the document in question. This can be indicated by the first person pronoun, but this is often left out and implied. A sentence should be considered first-person even if the author is only implied. The personal pronoun is often “jeg”, but can also be “vi” (PL) in cases where the document has several authors, or if it is a collective “vi” that really just indicates the evaluation of the author. There might be other indicators of first person as well, such as the author speaking of themself in the third person, etc.

      Det er ingen hemmelighet at nordmenn er et quiz-elskende folkeferd. [100122:3] (E, NFP, NOT)

In the above example, the ones having an evaluation towards "quiz" is "nordmenn" (Norwegians), not the author of the document. Sentences like this, where some general opinion is stated, can be quite common. The sentence is labeled as E because of ”-elskende”.

    Vi kommer veldig mye tettere på Ingemar Johansson enn vi gjør på Conor O´Malley. [400109:23] (E)

Here the pronoun "vi" (us) is used, but the holder of the evaluation is still the author of the article.

    
### Attribute: Topic relevance
A sentence is on topic, if the object being evaluated in a given sentence is the same as the object being reviewed in the document, an aspect/part of that object, or if the concept being evaluated includes the object of the review article. It is common for authors to write about other themes related to the product that they are reviewing. An example of the latter is if an author comments on all works belonging to an author being good, even though the article is only about *one* book. In such cases, if the sentences used are evaluative, they shall be labeled as not on topic (NOT). If a sentence is *on topic*, it is left unmarked. Common cases of NOT sentences include discussions about previous series or related movies, related themes, related products, personal history, and many more. Note that the word topic here is used to refer specifically to the reviewed object. In a movie review, if the author writes something evaluative about another movie, it is not on topic, even though they are both films. The evaluation has to be about the same object.

    Jeg likte den første sesongen av Frikjent ganske godt. [000335:4] (E, NOT)
    
In this example, the object being reviewed are the first four episodes of the second season of a TV-series. This sentence is  evaluative, but not on topic, and therefore it is labeled as: evaluative, not on topic (E, NOT).

### Attribute: Disagreement
This attribute is for curation only. Annotators should not assign this attribute to any sentences.

### Overlap
Sentences can sometimes contain more than one evaluation, separated by a conjunction, for example. In these cases we do not label all possibilities. If a sentence contains both E and E-FINP, it is labeled as E. If a sentence contains one evaluation on topic, and another not on topic, then the entire sentence is left unmarked, and likewise, if a sentence contains one evaluation in the first person, and another non-first-person sentence, then it is also left unmarked. 


# Part 2: Identifying the correct labels

### Sentence types
What sentences can be evaluative? Even if a “sentence” is not a sentence in the formal sense in terms of finite verbs and subjects, it can still be classified as evaluative. In practice this means that all headlines can be evaluative, such as:

    Variert og spennende [601625:1] (E)

### Less challenging sentences
It can help to think about three cases that are mostly evaluative:

#### Emotional sentences
Sentences including emotional responses (arousal) are very often evaluative. Words like *elske* (love),*like* (like),*hate* (hate), etc. can all be indicators of this. 

    Det kommer neppe som noen overraskelse at vi liker de trådløse Sennheiser Urbanite-modellene; de ser bra ut, virker solide, 
    og har et lydbilde vi liker. [202263:43] (E)

Here the word "liker" (likes) indicates a positive emotional evaluation.

    Jeg likte den første sesongen av Frikjent ganske godt. [000335:4] (E, NOT)

Same as above.

#### Rational evaluations with sentiment lexemes
These are sentences that are easy to see as positive/negative, but often lacking the arousal we find in emotional sentences. Types of sentences that belong to this category include those that indicate worth and utilitarian values. Key words include, but are not limited to, *nyttig* (useful), *verdt (penger,tid)* (worth (money, time)), etc.

    Variert og spennende [601625:1] (E)

A headline, but still evaluative, because of the two strongly evaluative adjectives "variert" (varied) and "spennende" (exciting).


    Sykdommer er nyttige fordi de bringer med seg en nødvendighet og et sett med spilleregler som umiddelbart er synlige for hvem 
    som helst, men de er også farlige som fortellermessig størrelse, fordi de kan enda opp med å bli en mekanisme mer enn noe 
    annet. [400109:8] (E, NOT)

Here the words "nyttige" (useful) and "farlige" (dangerous) indicate a positive and a negative evaluation of "sykdommer" (diseases). Note that this sentence is not on topic, the author only discusses the theme of the movie in question, not the movie itself.

    Hot Chip skiller seg ut fra de fleste andre populære elektronia-artistene i London. [601625:4] (E, NOT)

This sentence is evaluative, but not on topic. "Skille seg ut" (stand out) was seen to be evaluative and not provable, and slightly positive.

    Ivrig offensivt og grei kontroll bakover. [101115:12] (E)
    
"Ivrig" (eager) and "grei kontroll" (good control) indicate a positive evaluation.

    Hot Chip er utforskende og nyskapende, men kunne godt dratt den enda lenger når de først var på vei ut. [601625:12] (E)

This is an example of a sentence that has both positive and negative polarity.


####  Other gradable and relational adjectives
Other gradable adjectives also tend to indicate evaluations, because these adjectives are inherently subjective. Adjectives like *ekkel* (nasty) and *utmerket* (excellent) are examples of this. Relational adjectives such as *lang* (long), *stor* (big) and *liten* (small) tend to indicate some subjective evaluation, but can also be purely descriptive. 



### Evaluative Fact-Implied Non-Personal Sentence
Evaluative fact implied non-personal sentences (E-FINPs) are descriptive sentences, and should not include any explicit evaluative expressions like those discussed above. A sentence is labeled as E-FINP when it is a fact or descriptive sentence, the evaluation is implied and the sentence does not involve any personal experiences or judgements. E-FINPs are usually understood to be evaluative because we interpret them based on background knowledge in the field, or because of common (societal, cultural) knowledge. 
The stereotypical E-FINP is a completely factual sentence that carries no evaluation outside of the context it is found in. It is often some description, indication of the presence of some desired/undesired thing (without actually saying that the thing is, in fact, (un)desirable). A typical example would be *There is a pool* in a hotel review. Based on our knowledge of hotels, we know that this is usually a desirable fact. A test to check if a sentence is an E-FINP is to remove it from its context, and try to ignore common or field knowledge. If you still see it as evaluative, it is not a E-FINP. Consider the following example:

    Skrivehastigheten startet på 33 MB/sek og falt av mot i underkant av 20 MB/sek. [200014:13] (E-FINP)

This sentence has no adjectives, no other apparent sentiment lexemes, and is very descriptive. However, with our knowledge of the field (this is actually explained in the article), we understand that this sentence is an indication of the author's positive attitude towards the object. However, if we remove the sentence from context, it is not as clear. Therefore, we label it E-FINP.

Some other examples are:

    Med i esken følger det forøvrig også med en tradisjonell kabel med fjernkontroll på, og det betyr altså at du fortsatt kan 
    bruke hodetelefonene på gamlemåten med kabel om batteriet skulle gå tomt. [202263:25] (E-FINP)

Here there are no explicit indicators of evaluation, but based upon our common knowledge, we understand that the author writes this because it is a good thing. 

    Dette gir et gjennomsnitt på 27,3 MB/sek som er meget bra. [200014:14] (E)

The first part of this sentence would have been an E-FINP, but the comment makes the evaluation explicit and the sentence  evaluative.

In some cases, the author might write a sentence that has a clear E-FINP-like element in it, followed (or preceded) by a clear evaluation of that fact. The sentence is then labeled as E, following the rules stated in *Overlap* above.


The problem is usually between E-FINP, E and no evaluation at all. If the sentence stating facts, with no clear personal experience or inherently evaluative expression, but still clearly evaluative? Then it is probably an E-FINP.

### Subjective, but not evaluative
If the sentence is clearly subjective, but it is hard to decide whether it carries a positive or a negative evaluation, it might mean that the sentence is simply subjective, not evaluative. This can happen when discussing things that are inherently subjectively negative, but not evaluative. Death is generally a negative thing, but *His dog died* is not a negative evaluation. Some more examples are:
    
    Harry Hole får virkelig kjørt seg i Jo Nesbøs nye bok. [102138:7] (no evaluation)

Although the expression "får kjørt seg" is not stilistically neutral, and might feel subjective, it does not indicate an  *evaluation* in this sentence, and the sentence is not labeled.

    
    Amor blir en stund overvåket av politiet på sin vandring, og det virker som om de tolker alt han gjør og ikke gjør i verste mening. [500718:23] (no evaluation)

This sentence is taken from the author's synopsis of the play. It is a description of the play, but "tolker alt han gjør og ikke gjør i verste mening" seems negative and subjective. However, it is not evaluative. In these situations, it can help to consider the following: If there is an evaluation, what is the object of that evaluation? Is there enough info in the sentence to give a concrete description of the evaluation? In some cases, like here, the sentence is too vague or descriptive to count as evaluative.

### Modifiers
Be aware that modifiers can drastically change the evaluational value of a sentence. A sentence that would not be labeled as evaluative, might have been labeled if only one more word is added. These include words like *for*(too), *heldigvis* (fortunately), *uheldigvis* (unfortunately), *dessverre* (unfortunately) and *endelig*, (finally) among several others.

### Label guide summary

|Question|Label/Attribute|
|---|---|
|Is there an evaluative element in the sentence?|give label E|
|Is there an evaluative element, but also an E-FINP?|give label E|
|Is the only evaluative element an E-FINP?|give label E-FINP|

If any of the above are true, consider the following:

|Question|Label/Attribute|
|---|---|
|Is the whole sentence not first person?|add attribute NFP|
|Is the whole sentence not on topic?|add attribute NOT|


### Problems

Many sentences can be difficult to judge properly. We have tried to categorize and deal with some of the problems that may arise.
Some of the greatest challenges can be to distinguish whether a sentence is purely evaluative, evaluative fact-implied non-personal, or neither of these. 


## Special cases

### Sarcasm and Irony
Sarcastic or ironic sentences can be difficult to judge, but these tools may be used to indicate a type of evaluation. Be aware of whether the sentence actually contains some evaluation about something. Sentences

    Arbeidsledigheten kan ikke være stor når de tre måneder etter åpningen ikke har klart å  skaffe nok arbeidskraft, mente Robinson. [300016:15] (E-FINP)

This sentence is actually used to mean something along the lines of “The company is not working very hard at attracting employees”. Because the sentence superficially resembles a factual statement, it has been labeled as E-FINP. 

    Små barn vet ingenting om 90-tallet, og foreldrene var ferdig med å fly på disco i denne perioden. [100122:13] (E, NOT)

This sarcastic sentence has a negative evaluation of adult party habits. It was labeled as E, NOT, as the expression "fly på disco" was interpreted as a subjective evaluation of this habit. On the other hand, note that the first clause "små barn vet ingenting om 90-tallet", is considered E-FINP.

An example of an ironic sentence which was not labeled as evaluative, is the following pair:

    Hvem er målgruppen da? Unge, voksne som vil mimre tilbake? [100122:10-11] (no evaluation) (no evaluation)

Here it is implied something along the lines of “of course the target audience is not just young adults who want to 
    reminisce”, but it is not saying anything evaluatively positive or negative about them.

Examples of sentences that could also be labeled as evaluative, but of which we have not yet seen examples, are sentences like *Det var smart!* \[constructed example\] meaning “That was stupid”, etc.
 
### Exclamations and imperatives
Exclamations can be used to indicate evaluation, and should be labeled as such when they indicate positive or negative evaluation. Some examples are:


    Gi oss noe nytt! [100122:20] (E)

Here the exclamation indicates desire for something new, which indicates a negative evaluation of the current state of the  product (out of fashion). Evaluative.

    Se så lekre rødbeter! [300016:23] (E)

Here we have an exclamatory sentence with an imperative (urging the other to have a look), and a positive evaluation of the look of the red beets. Evaluative.

### Modality
Modal auxiliaries can pose difficulties for the annotator. Some projects chose to not annotate modal sentences and irrealis (see next subchapter), but we wish to annotate all sentences if they do convey evaluations. The following are some guidelines for problematic cases, but the annotator should be aware of unexpected variation.

#### Kunne (can,could)
In the present tense many sentences indicate hypothetical situations that do not necessarily indicate any evaluation. One example where *kunne* might indicate evaluation is in cases where the sentence indicates some ability or lack of it, as in: 

    Vi kan få vite hva som skjedde med Karina. [000335:15] (no evaluation)

Here, "kan" just adds an element of uncertainity.

#### Burde (should)
The use of burde in all tenses tends to indicate some evaluation. These sentences indicate that some aspect of the object being reviewed is not as it *should*, and that it *should* be some other way. Consider the following examples:

    Da bør du prøve Philips Fidelio X2 [202263:41] (E, NOT)
    
    
    Og de som er på jobb bør kunne legge veskene sine et annet sted enn godt synlig ved disken. [300016:16] (E)

    Før denne oppsetningen sendes ut på skoleturné, bør elevene gis en innføring i hva den dreier seg om. [500718:2] (E)

    Det burde være et av Elvebreddens største pre, særlig når de til overmål kaller seg matbar. [300016:11] (E)

    Temaet burde være godt nok i seg selv - hva er morsommere enn å høre og gjette på  gamle hits. [100122:8] (E)
    
The last sentence indicates that the theme by itself is not good enough, and should therefore be labeled as E.


### Irrealis
Like with modal auxiliaries, conditional sentences might also pose problems. Irrealis sentences, i.e. sentences that indicate hypothetical situations, are excluded by for example Toprak et al., but we wish to include them as long as they clearly indicate evaluations. A common way of using irrealis sentences to indicate (especially negative) evaluation, is to say that a certain thing *would have been* good *if* something were the case. This indicates that that aspect of the object is not satisfactory. Consider the following example:

    Bare Elvebredden får nok arbeidskraft og virkelig kan åpne matbaren gleder Robinson & Fredag seg til å komme tilbake. [300016:32] (E)

This says that elvebredden does not have enough workers and that the food bar is not really open. These can be seen as negative comments on the current situation. It also says that as long as these things are fixed, the rest of the restaurant is good enough, so that they would like to come back.

### Questions
Questions behave similarly to irrealis sentences. If a sentence questions some aspect of the object in question, in such a way that it clearly shows an evaluation, then it should be labeled as such.  

    Et «mimrespill» skal vel stimulere mer enn korttidsminnet? [100122:18] (E)
    
Here, the author indicates that the game in question does not "stimulere mer enn korttidsminnet" (stimulate more than the short-term memory).

    Vil du heller ha ren og klar hifi-lyd? Da bør du prøve Philips Fidelio X2 [202263:40-41] (E) (E, NOT)

Here we have two sentences. The first one is formulated as a question. It indicates that the product does not 
have "ren og klar hifi-lyd" (clean and clear hifi sound), and then the second sentence picks up on the first sentence and says that the other product has this positive feature.

### Comparative sentences
Comparative sentences is another category of special cases. What is special about comparative sentences is that they typically contain two evaluations. One is typically about the object of the review, while the other can be some related product. Typically, both sentences will have the same label, but one part will be on topic and one will be not on topic. If this is the case, remember that the sentence is *not* given the attribute NOT.

### Difficult lexemes
Sometimes it is simply difficult to judge whether a specific word is polar enough to make a sentence evaluative, or whether the sentence is neutral. Trust your own judgement. Some sentences are simply difficult to annotate, because people will view them differently. In some cases we might lack the background knowledge to be able to identify something as for example an E-FINP. In other cases we simply interpret a sentence in different, but equally plausible ways. Certain differences between annotators is to be expected. Remember to take note of difficult sentences so there is a chance to discuss these between annotators.

## Summary and tips

You can try asking yourself some questions to make it easier


<!--- tenker over at det er forskjell på polare og evaluative adjektiver. Noen får kun polaritet fra kontekst, mens noen får kun evaluasjon fra kontekst --->
|TIPS|LABELS|
|---|---|
|Does the sentence involve some clearly evaluative word?| -->E|
|Does the sentence describe a personal, positive or negative experience with the product?| -->E|
|Is the sentence describing an objective fact about the object being reviewed that is clearly positive or negative in the relative context?| --> E-FINP|
|Are there no personal experiences and no clearly evaluative words, but a clear evaluation?| --> E-FINP|
|Does the sentence clearly indicate the authors opinion about some object?| --> E|

### Test

Following is a short list of sentences where you can test your understanding of the annotation guidelines so far, with a short description of each sentence and the suggested labels. We urge the annotators to go through this list and decide upon labels and attributes for each sentence, before checking our suggestions below.

|SENTENCE|
|--------|
|(Music album) Samtidig virker musikken gjennomtenkt og detaljert.|
|(Video game) Dessuten har spillmakerne vært flinke til å tilføre nye, morsomme elementer som begrenser forutsigbarheten og gir hvert spill et unikt preg.|
|(Hard drive) Seagate Momentus finnes i størrelser fra 40 GB og oppover.|
|(Film series) Jeg likte den første sesongen av Frikjent ganske godt.|
|(Theater play) Så får han vite at en selvmordsbomber har sprengt seg i sentrum av byen.|
|(Restaurant) Robinson var like fornøyd med bitene av and servert med pære, valnøtter og västerbottenost.|
|(Headphone) Med i esken følger det forøvrig også med en tradisjonell kabel med fjernkontroll på, og det betyr altså at du fortsatt kan bruke hodetelefonene på gamlemåten med kabel om batteriet skulle gå tomt.|
|(Restaurant) Elvebredden annonserer på hjemmeside at konseptet er "norsk og nordisk innovativ mat basert på lokale produsenter og kortreiste råvarer som foredles og presenteres i et norsk designmiljø."|
|(Book) Det hele skrevet i et knapt, kontant og effektivt språk.|
|(Football game) Gult kort for filming allerede etter et kvarter.|
|(Restaurant) Jeg har aldri spist den oransje varianten av sorten, sa Fredag.|







### Suggested labels

|ID    |SENTENCE| LABEL AND EXPLANATION|
|------|--------|----------------------|
|601625:6|(Music album) Samtidig virker musikken gjennomtenkt og detaljert.|**E**. “Gjennomtenkt” and “detaljert” are generally evaluated to be positive words.
|100122:6|(Video game) Dessuten har spillmakerne vært flinke til å tilføre nye, morsomme elementer som begrenser forutsigbarheten og gir hvert spill et unikt preg.|**E**. The topic here are the series of the game, and since this includes the game, it is on topic. The words “flinke”, “morsomme”, and “unik” are evaluated to be positive.
|200014:25|(Hard drive) Seagate Momentus finnes i størrelser fra 40 GB og oppover.|**No evaluation**. This is merely a description of what is available on the market and should thus not be labeled.
|000335:4|(Film series) Jeg likte den første sesongen av Frikjent ganske godt.|**E, NOT**. “Likte” is generally a good indicator of an evaluative sentence, but it is not on topic as the review is about the second season.
|500718:18|(Theater play) Så får han vite at en selvmordsbomber har sprengt seg i sentrum av byen.|**No evaluation.** This is merely a description of what happens on stage and should thus not be labeled.
|300016:22|(Restaurant) Robinson var like fornøyd med bitene av and servert med pære, valnøtter og västerbottenost.|**E**. “Fornøyd” is a good indicator of a positive evaluated sentence, but it is not labeled as NFP because the author refers to himself in third person.
|202263:25|(Headphone) Med i esken følger det forøvrig også med en tradisjonell kabel med fjernkontroll på, og det betyr altså at du fortsatt kan bruke hodetelefonene på gamlemåten med kabel om batteriet skulle gå tomt.|**E-FINP**. This is a description of what is included with the headphone, but is seen as positive in the context that the headphone is wireless.
|300016:25|(Restaurant) Elvebredden annonserer på hjemmeside at konseptet er "norsk og nordisk innovativ mat basert på lokale produsenter og kortreiste råvarer som foredles og presenteres i et norsk designmiljø."|**E, NFP**. The holder is the restaurant and not the author, and thus labeled as NFP. Words like “innovativ” and “kortreist” are evaluated to be positive.
|102138:8|(Book) Det hele skrevet i et knapt, kontant og effektivt språk.|**E**. “Knapt” and “kontant” could very well have been negative words, but the use of “og” indicates that all three should have the same polarity, and since “effektivt” is overall positive, the sentence is evaluated to be positive.
|101115:42|(Football game) Gult kort for filming allerede etter et kvarter.|**E**. The use of “allerede” with something that is regarded as negative, here “gult kort”, makes the evaluation of the sentence negative.
|300016:24|(Restaurant) Jeg har aldri spist den oransje varianten av sorten, sa Fredag.|**No evaluation**. Even though this is clearly subjective, it is merely a statement and should thus not be labeled.




## References

Farah Benamara, Baptiste Chardon, Yannick Mathieu and Vladimir Popescu     
_Towards Context-Based Subjectivity Analysis_ ([pdf](https://aclweb.org/anthology/I11-1132))  
Proceedings of the 5th International Joint Conference on Natural Language Processing, pages 1180–1188    
Chiang Mai, Thailand, 2011

Bing Liu  
_Sentiment Analysis and Opinion Mining_ ([pdf](https://www.cs.uic.edu/~liub/FBS/SentimentAnalysis-and-OpinionMining.pdf), draft)  
Morgan & Claypool Publishers, Synthesis Lectures on Human Language Technologies, May 2012, Vol. 5, No. 1, pages 1–167

Bing Liu  
_Sentiment Analysis: mining sentiments, opinions, and emotions_  
Cambridge University Press, 2015

Christian Scheible and Hinrich Schütze  
_Sentiment Relevance_ ([pdf](https://www.aclweb.org/anthology/P13-1094))    
Proceedings of the 51st Annual Meeting of the Association for Computational Linguistics, pages 954–963    
Sofia, Bulgaria, 2013

Cigdem Toprak and Niklas Jakob and Iryna Gurevych  
_Sentence and Expression Level Annotation of Opinions in User-Generated Discourse_ ([pdf](https://www.aclweb.org/anthology/P/P10/P10-1059.pdf))    
Proceedings of the 48th Annual Meeting of the Association for Computational Linguistics, pages 575–584    
Uppsala, Sweden, 2010

Erik Velldal, Lilja Øvrelid, Eivind Alexander Bergem, Cathrine Stadsnes, Samia Touileb and Fredrik Jørgensen   
_NoReC: The Norwegian Review Corpus_ ([pdf](http://www.lrec-conf.org/proceedings/lrec2018/pdf/851.pdf))     
Proceedings of the 11th edition of the Language Resources and Evaluation Conference, pages 4186–4191  
Miyazaki, Japan, 2018
  
Richard Eckart de Castilho, Éva Mújdricza-Maydt, Seid Muhie Yimam, Silvana Hartmann, Iryna Gurevychm, Anette Frank and Chris Biemann  
_Web-based Tool for the Integrated Annotation of Semantic and Syntactic Structures_ ([pdf](http://aclweb.org/anthology/W16-4011.pdf))  
Proceedings of the LT4DH workshop at COLING 2016, pages 76-84  
Osaka, Japan, 2016  
