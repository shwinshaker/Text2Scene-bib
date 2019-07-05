# Text2Scene-bib
A list of materials related to text2scene

## 2D scene generation

* [Learning the Visual Interpretation of Sentences](LearningVisualInterpretationofSentences.pdf) (*ICCV-2013*)
  - **Target**: text -> Cartoon-like
  - **Method**: Statistical learning - Conditional Random Field (CRF)
  - **Dataset**: [Abstract Scene Dataset](https://vision.ece.vt.edu/clipart/)

* **[Text2Scene: Generating Compositional Scenes from Textual Descriptions](Text2Scene.pdf)** (*CVPR-2019*) #thorough
  - **Target**: text -> Cartoon-like scenes & Object layouts & Synthetic scenes
  - **Method**: End2end deep learning (Recurrent CNN + attention); Unified framework
  - **Dataset**: [Abstract Scene Dataset](https://vision.ece.vt.edu/clipart/); COCO
  - **Code**: [Text2Scene](https://github.com/uvavision/Text2Scene)

#### *Learn commonsense spatiotemporal knowledge*

* [Predicting Object Dynamics in Scenes](PredictingObjectDynamicsinScenes.pdf) (*CVPR-2014*)
  - **Target**: scene -> next scene
  - **Dataset**: [Abstract Scene Dataset](https://vision.ece.vt.edu/clipart/)
 
* [Visual Abstraction for Zero-Shot Learning](Zero-ShotlearningviaVisualAbstraction.pdf) (*ECCV-2014*)
  - **Target**: learn concepts involving individual poses and interations between two people
  - **Dataset**: Collected: two people interating via different verb phrases

* [Learning common sense through visual abstraction](LearningCommonSensethroughVisualAbstraction.pdf) (*ICCV-2015*)
  - **Target**: assess the plausibility of the interation in a scene
  - **Dataset**: Collected: indoor scenes


## 3D scene generation

#### [Stanford NLP group](https://nlp.stanford.edu/projects/text2scene.shtml)
* [Learning Spatial Knowledge for Text to 3D Scene Generation](Text23DSence-LearningSpatialKnowledge.pdf) (*EMNLP-2014*) #thorough
  - **Target**: Text -> 3D scene - room layout
  - **Method**: Mostly rule-based + Bayesian + NLP
  - **Dataset**: [Collected dataset of spatial relation descriptions](http://downloads.cs.stanford.edu/nlp/data/text2scene.shtml#lexground-acl2015)
  - Learned spatial relation mapping

* [Interactive Learning of Spatial Knowledge for Text to 3D Scene Generation
](InteractiveLearningofSpatialKnowledgeforTextto3DSceneGeneration.pdf) (*ACL-2014-Workshop*)
  - **Target**: Text -> 3D scene - room layout
  - **Method**: Interactive learning

* [Text to 3D Scene Generation with Rich Lexical Grounding](Textto3DSceneGenerationwithRichLexicalGrounding.pdf) (*ACL-2015*) #thorough
  - **Target**: Text -> 3D scene - room layout
  - **Method**: Mostly rule-based + Supervised learning -> learning lexical grounding (i.e. object match)
  - **Dataset**: [Collected dataset of scene-description pairs](http://downloads.cs.stanford.edu/nlp/data/text2scene.shtml#lexground-acl2015)


## Image synthesis

#### *GAN conditioned on text (Degrade on general images)*

* [Generative Adversarial Text to Image Synthesis](GenerativeAdversarialTexttoImageSynthesis.pdf) (*ICML-2016*)
  - **Target**: text -> photographic image (Bird & flower)
  - **Method**: Both generator and discriminator conditioned on text feature
  - **Dataset**: CUB dataset of bird images; Oxford-102 dataset of flower images
  - **Code**: [Generative Adversarial Text-to-Image Synthesis](https://github.com/reedscot/icml2016)

* [StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks](Zhang_StackGAN_Text_to_ICCV_2017_paper.pdf) (*ICCV-2017*)
  - **Target**: text -> photographic image (Bird & flower)
  - **Method**: two-stage GANs
  - **Dataset**: CUB; Oxford-102; MS-COCO
  - **Code**: [StackGAN](https://github.com/hanzhanggit/StackGAN)

#### *Utilize pixel-wise semantic labels*
* [Parallel multiscale autoregressive density estimation](ParallelMultiscaleAutoregressiveDensityEstimation.pdf) (*ICML-2017*)

#### *Semantic layout as intermediate representation OR Retrieval from oject database*

* [Semi-parametric Image Synthesis](Semi-parametricImageSynthesis.pdf) (*CVPR-2018*)
  - **Target**: Semantic layout -> Photographic image
  - **Method**:
    - Parametric + Non-parametric (segment retrieval)
    - Segment database -> **retrieve** -> composite -> resolve occlusion -> post-process
  - **Dataset**: Cityscapes; NYU; ADE20K (See *Datasets* in this paper)
  - **Code**: [SIMS](https://github.com/xjqicuhk/SIMS)
  - **Demo**: [Semi-parametric Image Synthesis](https://github.com/xjqicuhk/SIMS)

* [Image Generation from Scene Graphs](ImageGenerationfromSceneGraphs.pdf) (*CVPR-2018*)
  - **Target**: Scene graphs -> Photographic images
  - **Method**:
    - groud-truth object positions -> scene graphs
    - Graph processing: *graph convolution network*
    - symbolic graph -> scene layout: **bounding box & segmentation prediction**
    - scene layout -> image: *cascaded refinement network (CRN)*
    - image -> realistic image: adversarial training
  - **Dataset**:
    - [Visual Genome](https://visualgenome.org): Human annotated scene graphs provided
    - [COCO-Stuff](https://github.com/nightrome/cocostuff): COCO with pixel-level stuff annotations

* **[Inferring semantic layout for hierarchical text-to-image synthesis](Hong_Inferring_Semantic_Layout_CVPR_2018_paper.pdf)** (*CVPR-2018*)
  - **Target**: text -> photographic image
  - **Method**: text -> **semantic layout (box layout & shape)** -> image
  - **Dataset**: COCO


## Image retrieval

* [Image Retrieval Using Scene Graphs](ImageRetrievalusingSceneGraphs.pdf) (*CVPR-2015*)
  - **Target**: Textual query -> Semantically related image
  - **Method**: Scene graph; Conditional random field
  - **Dataset**: real-world scene graphs: manually labeled YFCC100m & COCO images

## Video scene generation
* [Imagine This! Scripts to Compositions to Videos](ImageThis_ScriptstoVideos.pdf) (*ECCV-2018*)
  - **Target**: text -> scene video
  - **Method**: Entity & Background retrieval + Layout composer
  - **Dataset**: FLINTSTONES: richly-annotated video-caption dataset
  - **Demo**: [CRAFT](https://youtu.be/688Vv86n0z8)




