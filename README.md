# SOTA - Multimodal Emotion Recognition and Emotional Ambiguity

### Main Contributions

:white_check_mark: State-of-the-art of databases used in **Multimodal Emotion Recognition** (MER) and comprised at least the visual and vocal modalities. 

:white_check_mark: Focus on the representation of **ambiguity in emotional models** for each database. We define emotional ambiguity as the difficulty for humans to identify, express and recognize an emotion with certainty.

### README Structure

1. [Emotional Models](#Emotional-Models): Brief summary of the discrete and continuous emotion representation
2. [Databases with Discrete Emotions](#Databases-with-Discrete-Emotions): General description and position with respect to the representation of emotional ambiguity
3. [Databases with Continuous Emotions](#Databases-with-Continuous-Emotions): General description and position with respect to the representation of emotional ambiguity

### Interested in my work?

Feel free to contact me at: helene.tran@etu.uca.fr

Please cite the following paper if our work is useful for your research:

```tex
@inproceedings{tran:hal-03485239,
  TITLE = {{L'ambigu{\"i}t{\'e} dans la repr{\'e}sentation des {\'e}motions : {\'e}tat de l'art des bases de donn{\'e}es multimodales}},
  AUTHOR = {Tran, H{\'e}l{\`e}ne and Brelet, Lisa and Falih, Issam and Goblet, Xavier and Mephu Nguifo, Engelbert},
  URL = {https://hal.archives-ouvertes.fr/hal-03485239},
  BOOKTITLE = {{Conf{\'e}rence Extraction et Gestion de Connaissances}},
  ADDRESS = {Blois, France},
  YEAR = {2022},
  MONTH = Jan,
  PDF = {https://hal.archives-ouvertes.fr/hal-03485239/file/EGC2022-article_final.pdf},
  HAL_ID = {hal-03485239},
  HAL_VERSION = {v1},
}
```

*The final version of our paper (in French) on the integration of emotional ambiguity in MER databases is being submitted to the 2022 French Speaking Conference on the Extraction and Management of Knowledge (EGC). We will update this README once the paper is publicly available.*

## Emotional Models

:link: Anchor Links:
1. [Discrete Model](#Discrete-Model): Description of discrete emotions and the main representations
2. [Continuous Model](#Continuous-Model): Description of continuous emotions and the main representations

### Discrete Model

Emotions are represented by discrete affective states. This approach is the most natural way for humans to define their own emotions. According to the evolutionary perspective, there are two main categories of emotions: 

* **Primary emotions** (or basic emotions): they are innate and universal emotions, short-lived and quickly triggered in response to an emotional stimulus. The list of primary emotions varies greatly depending on the discipline and the author. The most common ones are: 

  * The six primary emotions of Ekman (1992): fear, anger, joy, sadness, disgust and surprise. 

  * Plutchik (2001)'s Wheel of Emotions with eight primary emotions grouped into four pairs of opposing emotions: joy and sadness, confidence and disgust, fear and anger, anticipation and surprise. 



  <p font="italic" align="center">  

  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ce/Plutchik-wheel.svg/591px-Plutchik-wheel.svg.png" align="center" width="500" height="500">

  </p>

  
  <p font="italic" align="center"> 
  Plutchik's Wheel of Emotions
  </p>


* **Secondary emotions** (or complex emotions): they are derived from the feelings of the primary emotions, are acquired through learning and confrontation with reality, and are culture-dependent. As an example, after feeling anger, we may then feel shame or guilt. Secondary emotions are usually combinations of primary emotions (Nugier et al., 2009).

Primary emotions are frequently chosen as classes for the development of recognition models, thus avoiding a possible overlap of emotional states. Although the discrete approach remains widely favoured in research due to its intelligibility, limiting oneself to the recognition of a primary emotion is not sufficient to describe the whole spectrum of emotions.

[Go to top](#sota---multimodal-emotion-recognition-and-emotional-ambiguity)

### Continuous Model

Emotions are placed in a multidimensional space. A large majority of researchers working on the continuous model agree on the two following dimensions:

* **Valence** corresponds to the pleasantness of the emotion. For example, disgust is an unpleasant emotion and is therefore associated with a negative valence. In contrast, a positive valence is related to a pleasant emotion such as joy.

* **Arousal** (or activation) refers to the physiological intensity felt. Sadness, which leads to withdrawal, is associated with low activation. Anger activation is high because it releases an influx of energy that allows the individual to prepare for battle. 

 These two dimensions are not sufficient to characterize the emotion (e.g. both anger and fear have a negative valence and high arousal), hence the need of a third dimension. However, this one does not create a consensus in the research. 
 * According to Russell et Mehrabian (1977), it could correspond to **control**. Thus, an angry individual feels in control of the situation (positive control) while a person overwhelmed by sadness seems to see the situation slipping away (negative control). The resulting model is called PAD (Pleasure, Arousal, Dominance) and is sufficient to describe all emotions according to the authors.

  <p font="italic" align="center">  

  <img src="https://www.researchgate.net/profile/Sven-Buechel/publication/307512566/figure/fig2/AS:727675475873793@1550502761529/Positions-of-Ekmans-basic-emotions-within-the-emotional-space-spanned-by-the-Valence_W640.jpg" align="center" width="400" height="300">

  </p>

  
  <p font="italic" align="center"> 
  The Pleasure-Arousal-Dominance model (Source: Buechel et Hahn, 2016)
  </p>


  <p font="italic" align="center">  

  <img src="my-PAD.png" align="center" width="350" height="300" alt="PAD model french français">

  </p>

  
  <p font="italic" align="center"> 
  The Pleasure-Arousal-Dominance model, french version (based on Karg et al., 2013)
  </p>

  * According to Schlosberg (1954), it should be the **attention-rejection** dimension. Rejection is related to a strong attempt to exclude the external object, while attention is the active opposite of rejection.
 
  In addition to better temporal resolution, the continuous approach allows for a wide range of emotional states to be represented and for variations in these states over time to be handled (Gunes et al., 2011). These advantages have led to a growing interest in affective computing.

[Go to top](#sota---multimodal-emotion-recognition-and-emotional-ambiguity)
  


## Databases with Discrete Emotions

:link: Anchor Links:
1. [Description of the Databases](#Description-of-the-databases---Discrete): General information of the databases that have chosen discrete emotions 
2. [Databases and Emotional Ambiguity](#Databases-and-emotional-ambiguity---Discrete): Position of the databases with respect to the representation of emotional ambiguity

:triangular_flag_on_post: Databases marked with a * offer discrete and continuous representation of emotions.

### Description of the Databases - Discrete

Name | Year | Language | Modalities | Classes | Number sentences | Description
-----|------|----------|------------|---------|-----------------------|------------ 
 [CMU-MOSEAS](https://github.com/A2Zadeh/CMU-MultimodalSDK) ([paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8106386/)) | 2020 | French, Spanish, Portuguese, German | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise | 10000 per language | Monologue videos from YouTube. High diversity of topics covered by a large number of speakers. Annotations on sentiments, emotions, subjectivity and 12 personality traits. Each emotion annotated on a [0,3] Likert scale for its degree of presence.
 [CMU-MOSEI](https://github.com/A2Zadeh/CMU-MultimodalSDK) ([paper](https://aclanthology.org/P18-1208.pdf)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise | 23453 | Monologue videos from YouTube. High diversity of topics covered by a large number of speakers. Annotations on emotions and sentiments. Each emotion annotated on a [0,3] Likert scale for its degree of presence.
 [MELD](https://affective-meld.github.io/) ([paper](https://arxiv.org/pdf/1810.02508.pdf)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise, Neutral | 13708 | Clips from the TV series Friends. One of the largest databases involving more than two people in a conversation.
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2018 | English | Vocal, Visual, Textual | Happiness, Anger, Sadness, Fear, Disgust, Surprise, Neutral | 2400 | Monologue videos from YouTube. Uses gradual annotations with a focus on contextual emotion expressions.
 [RAVDESS](https://zenodo.org/record/1188976#.YKeFlqE69Pa) ([paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0196391)) | 2018 | English | Vocal, Visual | **For speech**: Calm, Happy, Sad, Angry, Fearful, Surprise, Disgust, Neutral ; **For song**: Calm, Happy, Sad, Angry, Fearful, Neutral | For each modality (vocal only, visual only, audio-visual): 1440 for speech, 1012 for song | Isolated sentences uttered by professional actors in studio. Designed for emotion recognition in speech and songs.
 [GEMEP](https://www.unige.ch/cisa/gemep) ([paper full set](https://www.unige.ch/cisa/files/5814/6721/0641/Banziger__Scherer_-_2010_-_Introducing_the_Geneva_Multimodal_Emotion_Portrayal_GEMEP_Corpus.pdf), [paper core set](https://d1wqtxts1xzle7.cloudfront.net/46181789/Introducing_the_Geneva_Multimodal_Expres20160602-24715-1im38pf-with-cover-page-v2.pdf?Expires=1634121969&Signature=JNTyURJDn7AnFpLMqDCg8K86MUAoKFrHlq5~nOGJ88CvCCUBDjfGmrpc26~7zzbv~RGVYlvJke2c-doHVFo-ELY-UGmZg4TzKc0LJlmJdW3d-dpu8COxXKrJFOANCHBeSfmc3ecyV~jXKtbB1VTyfl8f4uVky--2~IwvXabCK4OBQG8xE4Vm5KaVyZeXd0m5f7CFgI~VBn43ykH4i~2w0kmt0ad8AlDaTvySWiSKF0GNbQwC-4lASzCUyCAtduvGKvOLEvBAUzT8aiXCFy4LOx-0qRbYKIBRRdhv~OFt2Hh76mtkfCYbbXZJO9vvZ9McmeMSled0YTa~adqILYSLIA__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)) | 2010 | French | Vocal, Visual | Admiration, amusement, tenderness, anger, disgust, despair, pride, shame, anxiety, interest, irritation, joy, contempt, fear, pleasure, relief, surprise, sadness | 1260 (full set) / 154 (core set) portrayals[^no-info] | Professional actors playing out emotional scenarios. Emotions are chosen so that all the values of the valence-arousal pairs are represented (positive/negative valence, high/low arousal).
 [IEMOCAP](https://sail.usc.edu/iemocap/iemocap_release.htm)* ([paper](https://link.springer.com/article/10.1007/s10579-008-9076-6)) | 2008 | English | Vocal, Visual, Textual, Markers on face, head and hand | Happiness, Anger, Sadness, Neutral, Frustration | 10039 | Emotions are played out by professional actors. Widely used in affective computer research.
 [eNTERFACE'05](http://www.enterface.net/enterface05/docs/results/databases/project2_database.zip) ([paper](https://ieeexplore.ieee.org/abstract/document/1623803)) | 2006 | English | Vocal, Visual | Happiness, Anger, Sadness, Fear, Disgust, Surprise, Neutral | 1166 | Isolated sentences uttered by naive subjects from 14 nations. Mood induction by listening to short stories. Black background.

  [Go to top](#sota---multimodal-emotion-recognition-and-emotional-ambiguity)

### Databases and Emotional Ambiguity - Discrete

Name | Year | Final annotation | \# annotations per sentence | Aggregation of annotations
-----|------|------------------|------------------------------------|--------------------------
 [CMU-MOSEAS](https://github.com/A2Zadeh/CMU-MultimodalSDK) | 2020 | Many emotions possible per sentence | 3 | -
 [CMU-MOSEI](https://github.com/A2Zadeh/CMU-MultimodalSDK) | 2018 | Many emotions possible per sentence | 3 | -
 [MELD](https://affective-meld.github.io/) | 2018 | One emotion per sentence | 3 | Majority vote
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* | 2018 | One emotion per sentence | 5 | Majority vote
 [RAVDESS](https://zenodo.org/record/1188976#.YKeFlqE69Pa) | 2018 | One emotion per sentence with 2 intensities (normal, strong) | 10 | -
 [GEMEP](https://www.unige.ch/cisa/gemep) | 2010 | One or two emotion(s) per portrayal with 4 intensities (full set) / One emotion per portrayal with 5 intensities (core set) | 23 (audio-video), 23 (audio only), 25 (video only) | -
 [IEMOCAP](https://sail.usc.edu/iemocap/iemocap_release.htm)* | 2008 | One emotion per sentence | 3 | Majority vote
 [eNTERFACE'05](http://www.enterface.net/enterface05/docs/results/databases/project2_database.zip) | 2006 | One emotion per sentence | No annotation | -

  [Go to top](#sota---multimodal-emotion-recognition-and-emotional-ambiguity)

## Databases with Continuous Emotions

:link: Anchor Links:
1. [Description of the Databases](#Description-of-the-databases---Continuous): General information of the databases that have chosen continuous emotions
2. [Databases and Emotional Ambiguity](#Databases-and-emotional-ambiguity---Continuous): Position of the databases with respect to the representation of emotional ambiguity

:triangular_flag_on_post: Databases marked with a * offer discrete and continuous representation of emotions.

### Description of the Databases - Continuous

Name | Year | Language | Modalities | Dimensions | Number sentences | Description
-----|------|----------|------------|---------|-----------------------|------------ 
 [MuSe-CaR](https://zenodo.org/record/4651164#.YKUmHqE69hE) ([paper](https://dl.acm.org/doi/abs/10.1145/3423327.3423673)) | 2021 | English | Vocal, Visual, Textual | Valence, Arousal, Trustworthiness | 28295 | Car reviews from YouTube. In-the-wild characteristics (e.g. reviewer visibility, ambient noises, domain-specific terms). Designed for sentiment recognition, emotion-target engagement and trustworthiness detection.
 [SEWA](https://db.sewaproject.eu/) ([paper](https://ieeexplore.ieee.org/abstract/document/8854185)) | 2019 | English, German, Hungarian, Greek, Serbian, Chinese | Vocal, Visual, Textual | Valence, Arousal, Liking | 538[^sewa] | Ordinary people from the same culture discuss advertisements via video conference. Database created for emotion recognition but also for human behavior analysis, including cultural studies.
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2018 | English | Vocal, Visual, Textual | Valence, Arousal | 2400 | Monologue videos from YouTube. Uses gradual annotations with a focus on contextual emotion expressions.
 [RECOLA](https://diuf.unifr.ch/main/diva/recola/download.html) ([paper](https://drive.google.com/file/d/0B2V_I9XKBODhNENKUnZWNFdVXzQ/view?resourcekey=0-pkUwtWY7x82Gw5zurnQNag)) | 2013 | French | Vocal, Visual, ECG[^ecg], EDA[^eda] | Valence, Arousal | 3,8 hours[^no-info] | Online dyadic interactions where participants need to collaborate to solve a survival task. Mood Induction Procedure to elicit emotion.
 [SEMAINE](https://ieeexplore.ieee.org/abstract/document/5959155) ([paper](https://ieeexplore.ieee.org/abstract/document/8489099)) | 2012 | English | Vocal, Visual, Textual | Valence, Arousal, Dominance, Power, Intensity | 190 videos[^no-info] | Volunteers interact with an artificial character to which a personality trait has been assigned (angry, happy, gloomy, sensible).
 [IEMOCAP](https://sail.usc.edu/iemocap/iemocap_release.htm)* ([paper](https://link.springer.com/article/10.1007/s10579-008-9076-6)) | 2008 | English | Vocal, Visual, Textual, Markers on face, head and hand | Valence, Arousal, Dominance | 10039 | Emotions are played out by professional actors. Widely used in affective computer research. 
 SAL ([paper](https://mediatum.ub.tum.de/doc/980151/file.pdf)) | 2008 | English | Vocal, Visual | Valence, Arousal | 1692 turns[^no-info] | Natural human-SAL conversations involving artificial characters with different emotional personalities (angry, sad, gloomy, sensitive).
 [VAM](https://sail.usc.edu/VAM/vam_release.htm) ([paper](https://ieeexplore.ieee.org/abstract/document/4607572)) | 2008 | German | Vocal, Visual | Valence, Arousal, Dominance | 1018 | Videos from a German TV talk show: spontaneous emotions from unscripted discussion. Audio and face annotated separately.

[^sewa]: The paper does not specify whether it is all languages combined or a specific language.
[^ecg]: For Electrocardiogram 
[^eda]: For Electrodermal Activity
[^no-info]: No information provided on the number of annotated sentences. 

[Go to top](#sota---multimodal-emotion-recognition-and-emotional-ambiguity)


### Databases and Emotional Ambiguity - Continuous

Name | Year | Final annotation | \# annotations per sentence | Aggregation of annotations
-----|------|------------------|------------------------------------|--------------------------
 [MuSe-CaR](https://zenodo.org/record/4651164#.YKUmHqE69hE) | 2021 | Point in the emotional space | 5 | Evaluator Weighted Estimator
 [SEWA](https://db.sewaproject.eu/) | 2019 | Point in the emotional space | At least 3 | Canonical Time Warping
 [OMG-Emotions](https://github.com/knowledgetechnologyuhh/OMGEmotionChallenge)* | 2018 | Point in the emotional space | 5 | Evaluator Weighted Estimator
 [RECOLA](https://diuf.unifr.ch/main/diva/recola/download.html) | 2013 | Point in the emotional space | 6 | Mean Filtering
 [SEMAINE](https://ieeexplore.ieee.org/abstract/document/5959155) | 2012 | Point in the emotional space | 3 - 8 | -
 [IEMOCAP](https://sail.usc.edu/iemocap/iemocap_release.htm)* | 2008 | Single element from SAM[^sam] | 2 | Z-normalisation
 SAL | 2008 | Point in the emotional space | 4 | Z-normalisation
 [VAM](https://sail.usc.edu/VAM/vam_release.htm) | 2008 | Single element from SAM[^sam] | 6 - 17 (audio) ; 8 - 34 (face) | -

 [^sam]: SAM for [Self-Assessment Manikins](https://www.sciencedirect.com/science/article/abs/pii/0005791694900639)

 [Go to top](#sota---multimodal-emotion-recognition-and-emotional-ambiguity)


 ## References

 Buechel, S. et U. Hahn (2016).   Emotion Analysis as a Regression Problem — Dimensional Models and Their Implications on Emotion Representation and Metrical Evaluation. In *ECAI 2016*, pp.1114–1122. IOS Press. https://doi.org/10.3233/978-1-61499-672-9-1114

 Ekman, P. (1992). An Argument for Basic Emotions. *Cognition & Emotion 6*(3-4), 169–200. https://doi.org/10.1080/02699939208411068

 Gunes, H., B. Schuller, M. Pantic, et R. Cowie (2011).  Emotion representation, analysis and synthesis in continuous space : A survey.  In *2011 IEEE International Conference on Automatic Face & Gesture Recognition (FG)*, pp. 827–834. IEEE. https://doi.org/10.1109/FG.2011.5771357

 Karg, M., Samadani, A. A., Gorbet, R., Kühnlenz, K., Hoey, J., & Kulić, D. (2013). Body movements for affective expression: A survey of automatic recognition and generation. *IEEE Transactions on Affective Computing*, 4(4), 341-359.

 Nugier, A. (2009). Histoire et grands courants de recherche sur les émotions. *Revue électronique de Psychologie Sociale 4*(4), 8–14. https://doi.org/10.1109/FG.2011.5771357

 Plutchik, R. (2001). The Nature of Emotions : Human emotions have deep evolutionary roots, a fact that may explain their complexity and provide tools for clinical practice. *American Scientist 89*(4), 344–350. https://www.jstor.org/stable/27857503 

 Russell,  J.  A.  et  A.  Mehrabian  (1977).   Evidence  for  a  Three-Factor  Theory  of  Emotions. *Journal of Research in Personality 11*(3), 273–294. https://doi.org/10.1016/0092-6566(77)90037-X

 Schlosberg, H. (1954). Three dimensions of emotion. *Psychological Review, 61*(2), 81–88. https://doi.org/10.1037/h0054570
