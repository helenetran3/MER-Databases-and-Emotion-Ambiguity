# SOTA-Multimodal-Emotion-Recognition

State-of-the-art of databases used in **Multimodal Emotion Recognition** and comprised at least the visual and vocal modalities. 

We also propose a focus on the representation of **ambiguity in emotional models** for each database. We define emotional ambiguity as the difficulty for humans to identify, express and recognize an emotion with certainty.

In the following, databases will be divided into two categories: those with a [discrete representation](#Discrete-Emotion-Representation) and those with a [continuous representation](#Continuous-Emotion-Representation). Databases marked with a * offer both approaches.

## Discrete Emotion Representation

This section present the general information of the databases that have chosen a discrete representation of emotions ([Description of the Databases](#Description-of-the-databases---Discrete) subsection). The table listing the criteria for introducing ambiguity into the discrete emotion representation can be found in the [Databases and Emotional Ambiguity](#Databases-and-emotional-ambiguity---Discrete) subsection.

### Description of the Databases - Discrete

Name | Year | Language | Modalities | Classes | Number sentences | Description
-----|------|----------|------------|---------|-----------------------|------------ 
 [CMU-MOSEAS](https://github.com/A2Zadeh/CMU-MultimodalSDK) ([paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8106386/)) | 2020 | French, Spanish, Portuguese, German | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise | 10000 per language | Monologue videos from YouTube. High diversity of topics covered by a large number of speakers. Annotations on sentiments, emotions, subjectivity and 12 personality traits. Each emotion annotated on a [0,3] Likert scale for its degree of presence.
 [CMU-MOSEI](https://github.com/A2Zadeh/CMU-MultimodalSDK) ([paper](https://aclanthology.org/P18-1208.pdf)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise | 23453 | Monologue videos from YouTube. High diversity of topics covered by a large number of speakers. Annotations on emotions and sentiments. Each emotion annotated on a [0,3] Likert scale for its degree of presence.
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise, Neutral | 2400 | Monologue videos from YouTube. Uses gradual annotations with a focus on contextual emotion expressions.
 [MELD](https://affective-meld.github.io/) ([paper](https://arxiv.org/pdf/1810.02508.pdf)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise, Neutral | 13708 | Clips from the TV series Friends. One of the largest databases involving more than two people in a conversation.
 [IEMOCAP](https://sail.usc.edu/iemocap/iemocap_release.htm)* ([paper](https://link.springer.com/article/10.1007/s10579-008-9076-6)) | 2008 | English | Vocal, Visual, Textual, Markers on face, head and hand | Happiness, Anger, Sadness, Neutral, Frustration | 10039 | Emotions are played out by professional actors. Widely used in affective computer research.



### Databases and Emotional Ambiguity - Discrete

Name | Year | Final annotation | \# annotations per sentence | Aggregation of annotations
-----|------|------------------|------------------------------------|--------------------------
 [CMU-MOSEAS](https://github.com/A2Zadeh/CMU-MultimodalSDK) | 2020 | Many emotions possible per sentence | 3 | Not reported
 [CMU-MOSEI](https://github.com/A2Zadeh/CMU-MultimodalSDK) | 2018 | Many emotions possible per sentence | 3 | Not reported
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* | 2018 | One emotion per sentence | 5 | Majority vote
 [MELD](https://affective-meld.github.io/) | 2018 | One emotion per sentence | 3 | Majority vote
 [IEMOCAP](https://sail.usc.edu/iemocap/iemocap_release.htm)* | 2008 | One emotion per sentence | 3 | Majority vote



## Continuous Emotion Representation

This section present the general information of the databases that have chosen a continuous representation of emotions ([Description of the Databases](#Description-of-the-databases---Continuous) subsection). The table listing the criteria for introducing ambiguity into the continuous emotion representation can be found in the [Databases and Emotional Ambiguity](#Databases-and-emotional-ambiguity---Continuous) subsection.

### Description of the Databases - Continuous

Name | Year | Language | Modalities | Dimensions | Number sentences | Description
-----|------|----------|------------|---------|-----------------------|------------ 
 [MuSe-CaR](https://zenodo.org/record/4651164#.YKUmHqE69hE) ([paper](https://dl.acm.org/doi/abs/10.1145/3423327.3423673)) | 2021 | English | Vocal, Visual, Textual | Valence, Activation, Trustworthiness | 28295 | Car reviews from YouTube. In-the-wild characteristics (e.g. reviewer visibility, ambient noises, domain-specific terms). Designed for sentiment recognition, emotion-target engagement and trustworthiness detection.
 [SEWA](https://db.sewaproject.eu/) ([paper](https://ieeexplore.ieee.org/abstract/document/8854185)) | 2019 | English, German, Hungarian, Greek, Serbian, Chinese | Vocal, Visual, Textual | Valence, Activation, Liking | 538[^SEWA] | Ordinary people from the same culture discuss advertisements via video conference. Database created for emotion recognition but also for human behavior analysis, including cultural studies.
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2018 | English | Vocal, Visual, Textual | Valence, Activation | 2400 | Monologue videos from YouTube. Uses gradual annotations with a focus on contextual emotion expressions.
 [SEMAINE](https://ieeexplore.ieee.org/abstract/document/5959155) ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2012 | English | Vocal, Visual, Textual | Valence, Arousal, Dominance, Power, Intensity | 190 videos[^SEMAINE] | Volunteers interact with an artificial character to which a personality trait has been assigned (angry, happy, gloomy, sensible).
[IEMOCAP](https://sail.usc.edu/iemocap/iemocap_release.htm)* ([paper](https://link.springer.com/article/10.1007/s10579-008-9076-6)) | 2008 | English | Vocal, Visual, Textual, Markers on face, head and hand | Valence, Arousal, Dominance | 10039 | Emotions are played out by professional actors. Widely used in affective computer research. 

[^SEWA]: The paper does not specify whether it is all languages combined or a specific language.
[^SEMAINE]: No information provided on the number of annotated sentences. 


### Databases and Emotional Ambiguity - Continuous

Name | Year | Final annotation | \# annotations per sentence | Aggregation of annotations
-----|------|------------------|------------------------------------|--------------------------
 [MuSe-CaR](https://zenodo.org/record/4651164#.YKUmHqE69hE) | 2021 | Point in the emotional space | 5 | Evaluator Weighted Estimator
 [SEWA](https://db.sewaproject.eu/) | 2019 | Point in the emotional space | At least 3 | Canonical Time Warping
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* | 2018 | Point in the emotional space | 5 | Evaluator Weighted Estimator
 [SEMAINE](https://ieeexplore.ieee.org/abstract/document/5959155) | 2012 | Point in the emotional space | From 6 to 8 | Not reported
 [IEMOCAP](https://sail.usc.edu/iemocap/iemocap_release.htm)* | 2008 | Single element from SAM[^IEMOCAP] | 2 | Z-normalisation

 [^IEMOCAP]: SAM for [Self-Assessment Manikins](https://www.sciencedirect.com/science/article/abs/pii/0005791694900639)