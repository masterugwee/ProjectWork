
### Detection of Hospital Acquired Infections in sparse and noisy Swedish patient records

#### Summary

This paper is written by a team of students in Stockholm University. Their aim was to build a system which could reliably
retrieves all patient records which potentially include HAI,
.to reduce the burden of manually checking patient records
by the hospital staff.This paper focuses on deploying three machine learning
algorithms to hospitalization records. The study was of an experimantal nature, using  Naıve Bayes (NB), Support Vector Machines (SVM) and a C4.5 Decision Tree to the
problem and the evaluation of the efficiency of this approach. The data set available to the team was considered noisy which means the data was handwritten which had spelling mistakes, abbreviations, and non-standard terminology or missing punctuation.  The data included patient records,newspaper articles and blogs.

Research on the detection of HAI(Hospital Acquired Infections) was done using
crobiological data, antimicrobial criteria and diagnosis codes. This could help in identifying central line-associated bloodstream infections, surgical site
infections, and VAP.The authors try to detect HAI by applying a SVM to patient records provided by the University Hospital of Geneva.Na¨ıve Bayes yielded maximum performance level, 87% recall and 74% specificity of all classifiers tested as well
as for all resampling preprocessing experiments.

The team decided to merge all daily patient records which
belong to one hospitalization into one file, which we will call
Hospitalization Records (HSR).The time frame is based on international definitions
of HAI and the incubation period of infections and is estimated to be less than 48 hours for a multitude of disorders.
This procedure yielded a total of 213 PPM-HSRs (Point
Prevalence Measures) of which 128 contain HAI and 85 do not. This is the data we use as input for the classifiers in our current study.

##### Techniques used

 ###### Stop word removal:-
 The team were able to
apply a filter which removed all stop words from the input
text at the same time we ran the StringToWordVector

###### Infection-specific terms (IST):-  
The medical experts involved in this project supplied a seed set of about 30 infection-specific terms; these
were based on frequent observations in the data as well as the
experts’ knowledge about infections. The seed set was then
extended by finding related terms, e.g., synonyms or misspellings of the input term, through the use of an automatic
synonym generator.

###### Term Frequency-Inverse Document Frequency:- 
A mechanism used in combination with TF, to attenuate the effect of words that occur too often in the set of documents as that they could be
important in order to discriminate between those. IDF is
calculated as follows: idft = log N
dft where N is the number of documents in a collection and dft is the document
frequency of term t, i.e. the number of documents in the
collection that contain t. TF-IDF for a term is calculated
by: tf idft,d = tft,d × idft. Thus, TF-IDF for a t is highest
if t occurs many times within a small number of documents.

##### Evaluation

###### 10-fold cross-validation:- 
stratified 10-
fold cross-validation, one of the best known and most commonly used evaluation techniques, was used.

###### Statistical tests:-  
statistical testing
is necessary in order to verify the significance of the results.

##### Results

###### SVM (TF-IDF 50)
obtains the highest recall with a
slightly lower overall performance.( 76.7%)

###### SVM (no preprocessing)
shows the overall best performance, having yet a considerable lower recall(78.6%).
