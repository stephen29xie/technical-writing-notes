# technical-writing-notes

Personal notes to improve technical writing.

References:
  
  * https://developers.google.com/tech-writing/one

## Words

* Define new or unfamiliar terms

  If the term already exists, link to a good explanation. Do not reinvent the wheel
  If your document is introducing the term, define the term. If you are introducing many terms, collect into a glossary
 
* Use the same unambiguous work or term consistently throughout your document. Don't rename it.

* If using an acryonym, spell out the full name and ancronym in bold (Eg. **Telekenetic Tactile Network (TTN)**). Then you may use the acryonym going forward. Do not cycle between the full name and acryonym. Use one.

* Only define acronyms if the acronym is significantly shorter than the full term, and it will be used many times

* Disambiguate pronouns. **It, they, them, their, this** and **that** can cause a lot of confusion. Make sure it is clear what noun the pronoun is representing, or just resuse the noun and don't use a pronoun.

## Active Voice vs. Passive Voice

* The majority of sentences in technical writing should be in **active voice**, as opposed to **passive voice**. In an active voice sentence, an actor acts on a target (sentece = actor + verb + target). In a passive voice sentence, it is the reverse (sentence = target + verb + actor). Eg. The cat sat on the mat vs. The mat was sat on by the cat.

* Prefer active voice to passive voice. Be bold - be active.

## Clear Sentences

* Choose strong verbs. Reduce imprecise, weak, or generic verbs such as: forms of be (is, are, am, was, were), occur, happen.

* Reduce there is/there are. Replacing **There are** with **you** strengthens the sentence.

* Minimize certain adjectives and adverbs. Adjectives and adverbs perform amazingly well in fiction and poetry. But adjectives and adverbs tend to be too loosely defined and subjective for technical readers. Worse, adjectives and adverbs can make technical documentation sound dangerously like marketing material. Feed your technical readers factual data instead of marketing speak. For example:

  > Setting this flag makes the application run screamingly fast.

  > Setting this flag makes the application run 225-250% faster.

## Short sentences

* Focus each sentence on a single idea.

* Convert some long sentences into lists. When you see a conjunction **or** in a sentence, consider refactoring into a bulleted list.

* Eliminate or reduce extraneous words

* Reduce subordinate clauses. Scrutinize subordinate clauses and keep the `one sentence = one idea` formula in mind. Do the subordinate clauses in a sentence _extend_ the single idea or do they _branch off_ into a separate idea. If the latter, consider dividing the offending subordinate clause(s) into a separate sentences.

  ```
  Python is an interpreted programming language, which was invented in 1991.
    
    * main clause: Python is an interpreted programming language
    * subordinate clause: which was invented in 1991
  ```

* Distinguish **that** from **which**: Use **which** for nonessential subordinate clauses, and use **that** for an essential subordinate clause that the sentence cannot live without.  Place a comma before **which**; do not place a comma before **that**. Examples:

  > Python is an interpreted language, **which** Guido van Rossum invented
  
  > Fortran is perfect for mathematical calculations **that** don't involve linear algebra

## Lists and Tables

* Lists provide something orderly. Choose the correct type of list. There are:
   * bulleted lists, for unordered items
   * numbered lists, for ordered items
   * embedded lists contains items stuffed within a sentence, and generally speaking, are a poor choice. Try to transform into an bulleted or numbered list.

* Keep list items parallel, which means all items match along the following parameters:
  * grammar
  * logical category
  * capitalization
  * punctuation
  
  The first item in a list establishes a pattern that readers expect to see repeated in subsequent items.
  
* Start numbered lists with an imperative verb. An imperative verb is a command, such as **open** or **start**.

* If a list item is a sentence, use sentence capitalization and punctuation. Otherwise, do not use capitalization or punctuation.

* Create useful tables. Consider the following guidelines:
  * Label each column with a meaningful header.
  * Avoid putting too much text into a table cell. If a cell holds more than 2 sentences, ask yourself whether that info belongs in another format.
  * Strive for parallelism _within_ individual columns.

* Introduce each list and table with a sentence that tells readers what the list of table represents. Terminate the introductory sentence with a colon, rather than a period. Recommendation: put the word **following** into the introductory sentence. Examples:
  > The following list identifies key performance parameters:
  
  > Take the following steps to install the Frambus package:

## Paragraphs

* The opening sentence is the most important sentence of any paragraph. Good opening sentences establish the paragraph's central point.

* Focus each paragraph on a single topic. Don't describe what will happen in a future topic or what happened in a past topic. When revising, ruthlessly delete (or move to another paragraph) any sentence that doesn't directly relate to the current topic.

* Don't make paragraphs too long or too short. Readers generally welcome paragraphs containing 3 to 5 sentences, and avoid paragraphs more than about 7 sentences. Consider diving long paragraphs into two separate paragraphs. Conversely, if your document contains plenty of one-sentence paragraphs, your organization is faulty. Seek ways to combine those one-sentence paragraphs into cohesive multi-sentence paragraphs or possibly into lists.

* Answer what, why and how. Good paragraphs answer the following three sentences:
  1. **What** are you trying to tell the reader?
  
  2. **Why** is it important for the reader to know this?
  
  3. **How** should the reader use this knowledge. Alternatively, how should the reader know your point to be true?

## Audience

* Make sure your document provides the information your audience needs that your audience doesn't already have. Targetting the _wrong_ audience can be messy.

* Define your audience. Begin by identifying your audience's **role(s)**. Roles remain an essential first-order approximation in defining your audience. People in the same role _generally_ share certain base skills and knowledge. But roles, by themselves, are insufficient for defining an audience. You must also consider your audience's _proximity_ to the knowledge. Time also affects proximity. For example, almost all software engineers studied calculus. However, most software engineers don't use calculus in their jobs so their knowledge of calculus gradually fades.

* Determine what your audience needs to learn. Write down a list of everything your target audience needs to learn to accomplish goals. In some cases, the list should hold tasks that the target audience needs to _perform_. For example:

  ```
  After reading the documentation, the audience will know how to do the following tasks:
    
    * Use the Zylmon API to list hotels by price.
    * Use the Zylmon API to list hotels by location.
    * Use the Zylmon API to list hotels by user ratings.
  ```
  or

  ```
  After reading design spec, the audience will learn the following:
    
    * Three reasons by Zylmon outperforms Zyljeune.
    * Five reasons by Zylmon consumed 5.25 engineering years to develop.
  ```

  Note that your audience must sometimes master tasks in a certain order.

* Fit documentation to your audience. You must create explanations that satisfy your audience's curiosity rather than your own. Here are some key parameters to focus on:

  * Vocabulary and concepts: Be mindful of proximity. Do you expect your target audience to understand the abbreviations and vocabulary you are using?
  * Curse of knowledge: As experts, it is easy to forget that novices don't know what you already know.
  * Simple words: English has become the dominant language for technical communication worldwide. However, a significant percentage of technical readers are more comfortable in languages other than English. Therefore, prefer simple words over complex words.
  * Cultural neutrality and idioms. Keep your writing culturally neutral. Do not require readers to understand idioms. Example: `a piece of cake`.

## Documents

* State your document's scope. A good document begins by defining its scope. For example:
  
  > This document describes the overall design of Project Frambus
  
  A better document additionally defines its non-scope - the topics not covered that the target audience might expect. For example:
  
  > This document does not describe the design for the related technology, Project Froobus.

* State your audience. A good document explicitly specifies its audience. For example:

  > I wrote this document for the test engineers supporting Project Frambus.

  A good audience declaration might also specify any prerequisite knowledge or experience. For example:
  
  > This document assumes that you understand matrix multiplication and how to brew a really good cup of tea.

  In some cases, the audience declaration might also specify prerequisite documents. For example:
  
  > You must read "Project Froobus: A New Hope" prior to reading this document.

* Establish your key points up front. Imagine that your peers might only read the first paragraph of page one. Ensure the start of your document answers all of your readers' essential questions. Always write a summary for long engineering documents.

* Write for your audience. For example, answering the following questions helps you determine what your document should contain:

    * Who is your target audience?
    * What do your readers already know before they read your document?
    * What should your readers know or be able to do after they read your document?

    For example, suppose you have invented a new sorting algorithm. The following list contains some potential answers to the preceding questions:
    
    ```
    * My target audience is all the software engineers in my organization.
    
    * Before reading, most of my target audience studied sorting algorithms in school. However, about 25% of my target audience hasn't implemented or evaluated a sorting algorithm in many years.
    
    * After reading this document, my target audience will be able to do all of the following:
      * Implement the algorithm in their choice of programming language.
      * Identify the two kinds of datasets for which the algorithm outperforms the quicksort algorithm.
      * Identify the two edge cases in which the algorithm performs poorly.
    ```
    
    After defining the audience, organize the document to supply what readers should know or be able to do after reading the document. For example, the outline for the document could look as follows:
    
    ```
    1. Overview of the algorithm
      a. Comparison to quicksort
      b. Big O comparison: quicksort vs. new algorithm
    
    2. Implementations
      a. Implementation in pseudocode
      b. Implementation tips
    
    3. Deeper analysis of algorithm
      a. Optimal datasets
      b. Edge case problems
    ```
    
* Break your topic into sections. 
  
## Punctuation

* Semicolons: A period separates distinct thoughts; semicolon unites highly related thoughts. For example:
  
  > Rerun Frambus after updating your configuration file; don't rerun Frambus after updating existing source code.

* Em-Dashes: An em-dash represents a long pause-a bigger break-than a comma. For example:

  > C++ is a rich language-one requiring extensive experience to master.

  Writers sometimes use a pair of em-dashes to block off a digression. For example:
  
  > Protocol buffers-often nicknamed protobufs-encode structured data in an efficient yet extensible format.

* Parentheses: Use parentheses to hold minor points and digressions. Text enclosed in parentheses isn't critical. Keep parentheses to a minimum in technical writing.







