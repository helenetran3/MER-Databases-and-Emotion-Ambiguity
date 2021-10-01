# SOTA-Multimodal-Emotion-Recognition

Here is a state-of-the-art of databases used in **Multimodal Emotion Recognition** and comprised at least the facial and vocal modalities. 

A focus on the representation of **emotional ambiguity** in these databases is made. Emotional ambiguity is defined as the difficulty for humans to identify, express and recognize an emotion with certainty.

Databases are divided into two categories: those with a discrete representation of emotions and those with a continuous representation. Databases marked with a * offer both approaches.

## Discrete Emotion Representation

### Description of the databases

The table listing the criteria for emotional ambiguity representation can be found [in this subsection](#Databases-and-emotional-ambiguity-(D)).

Name | Year | Language | Modalities | Classes | Number sentences | Description
-----|------|----------|------------|---------|-----------------------|------------ 
 [CMU-MOSEAS](https://github.com/A2Zadeh/CMU-MultimodalSDK) ([paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8106386/)) | 2020 | French, Spanish, Portuguese, German | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise | 10000 per language | Monologue videos from YouTube. High diversity of topics covered by a large number of speakers. Annotations on sentiments, emotions, subjectivity and 12 personality traits. Each emotion annotated on a [0,3] Likert scale for its degree of presence.
 [CMU-MOSEI](https://github.com/A2Zadeh/CMU-MultimodalSDK) ([paper](https://aclanthology.org/P18-1208.pdf)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise | 23453 | Monologue videos from YouTube. High diversity of topics covered by a large number of speakers. Annotations on emotions and sentiments. Each emotion annotated on a [0,3] Likert scale for its degree of presence.
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise, Neutral | 2400 | Monologue videos from YouTube. Uses gradual annotations with a focus on contextual emotion expressions.
 [MELD](https://affective-meld.github.io/) ([paper](https://arxiv.org/pdf/1810.02508.pdf)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise, Neutral | 13708 | Clips from the TV series Friends. One of the largest databases involving more than two people in a conversation.
 IEMOCAP* ([paper](https://link.springer.com/article/10.1007/s10579-008-9076-6)) | 2008 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Neutral, Frustration | 10039 | Emotions are played out by professional actors. Widely used in affective computer research.



### Databases and emotional ambiguity (D)

Name | Year | Final annotation | \# annotations per sentence | Aggregation of annotations
-----|------|------------------|------------------------------------|--------------------------
 [CMU-MOSEAS](https://github.com/A2Zadeh/CMU-MultimodalSDK) | 2020 | Many emotions possible per sentence | 3 | Not reported
 [CMU-MOSEI](https://github.com/A2Zadeh/CMU-MultimodalSDK) | 2018 | Many emotions possible per sentence | 3 | Not reported
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* | 2018 | One emotion per sentence | 5 | Majority vote
 [MELD](https://affective-meld.github.io/) | 2018 | One emotion per sentence | 3 | Majority vote
 IEMOCAP* | 2008 | One emotion per sentence | 3 | Majority vote



## Continuous Emotion Representation

The table listing the criteria for emotional ambiguity representation can be found [in this subsection](#Databases-and-emotional-ambiguity-(C)).

Name | Year | Language | Modalities | Classes | Number sentences | Description
-----|------|----------|------------|---------|-----------------------|------------ 
 [MuSe-CaR](https://zenodo.org/record/4651164#.YKUmHqE69hE) ([paper](https://dl.acm.org/doi/abs/10.1145/3423327.3423673)) | 2021 | English | Vocal, Visual, Textual | Valence, Activation, Trustworthiness | 28295 | Car reviews from YouTube. In-the-wild characteristics (e.g. reviewer visibility, ambient noises, domain-specific terms). Designed for sentiment recognition, emotion-target engagement and trustworthiness detection.
 [SEWA](https://db.sewaproject.eu/) ([paper](https://ieeexplore.ieee.org/abstract/document/8854185)) | 2019 | English, German, Hungarian, Greek, Serbian, Chinese | Vocal, Visual, Textual | Valence, Activation, Liking | 538[^SEWA] | Ordinary people from the same culture discuss advertisements via video conference. Database created for emotion recognition but also for human behavior analysis, including cultural studies.
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2018 | English | Vocal, Visual, Textual | Valence, Activation | 2400 | Monologue videos from YouTube. Uses gradual annotations with a focus on contextual emotion expressions.
 [SEMAINE](https://ieeexplore.ieee.org/abstract/document/5959155) ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2012 | English | Vocal, Visual, Textual | Valence, Arousal, Dominance, Power, Intensity | 190 videos[^SEMAINE] | Volunteers interact with an artificial character to which a personality trait has been assigned (angry, happy, gloomy, sensible).
IEMOCAP* ([paper](https://ieeexplore.ieee.org/abstract/document/5959155)) | 2008 | English | Vocal, Visual, Textual | Valence, Arousal, Dominance | 10039 | Emotions are played out by professional actors. Widely used in affective computer research. 

[^SEWA]: The paper does not specify whether it is all languages combined or a specific language.
[^SEMAINE]: No information provided on the number of annotated sentences. 


### Databases and emotional ambiguity (C)

Name | Year | Final annotation | \# annotations per sentence | Aggregation of annotations
-----|------|------------------|------------------------------------|--------------------------
 [MuSe-CaR](https://zenodo.org/record/4651164#.YKUmHqE69hE) | 2021 | Point in the emotional space | 5 | Evaluator Weighted Estimator
 [SEWA](https://db.sewaproject.eu/) | 2019 | Point in the emotional space | At least 3 | Canonical Time Warping
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* | 2018 | Point in the emotional space | 5 | Evaluator Weighted Estimator
 [SEMAINE](https://ieeexplore.ieee.org/abstract/document/5959155) | 2012 | Point in the emotional space | From 6 to 8 | Not reported
 IEMOCAP* | 2008 | Single element from SAM[^IEMOCAP] | 2 | z-normalisation

 [^IEMOCAP]: SAM for [Self-Assessment Manikins](https://www.sciencedirect.com/science/article/abs/pii/0005791694900639)