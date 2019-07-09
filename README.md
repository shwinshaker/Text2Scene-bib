# Text2Scene-bib
A list of materials related to text2scene

## Dataset investigation
* Abstract Scene Dataset (*[CVPR-2013](AbstractScene/AbstactSceneDataset.pdf) & [PAMI-2015](AbstractScene/AbstactSceneDataset-new.pdf)*) #thorough

## Abstract scene generation

* **[Learning the Visual Interpretation of Sentences](AbstractScene/LearningVisualInterpretationofSentences.pdf)** (*ICCV-2013*)
  - **Target**: text -> Cartoon-like
  - **Method**: Statistical learning - Conditional Random Field (CRF)
  - **Dataset**: [Abstract Scene Dataset](https://vision.ece.vt.edu/clipart/)
  - [Supplementary Material](LearningVisualInterpretationofSentences-SupplementaryMaterial.pdf)

* **[Text2Scene: Generating Compositional Scenes from Textual Descriptions](AbstractScene/Text2Scene.pdf)** (*CVPR-2019*) #thorough
  - **Target**: text -> Cartoon-like scenes & Object layouts & Synthetic scenes
  - **Method**: End2end deep learning (Recurrent CNN + attention); Unified framework
  - **Dataset**: [Abstract Scene Dataset](https://vision.ece.vt.edu/clipart/); COCO
  - **Code**: [Text2Scene](https://github.com/uvavision/Text2Scene)

#### *Learn commonsense spatiotemporal knowledge*

* [Predicting Object Dynamics in Scenes](AbstractScene/PredictingObjectDynamicsinScenes.pdf) (*CVPR-2014*)
  - **Target**: scene -> next scene
  - **Dataset**: [Abstract Scene Dataset](https://vision.ece.vt.edu/clipart/)
 
* [Visual Abstraction for Zero-Shot Learning](AbstractScene/Zero-ShotlearningviaVisualAbstraction.pdf) (*ECCV-2014*)
  - **Target**: learn concepts involving individual poses and interactions between two people
  - **Dataset**: Abstract scenes depicting fine-grained iteractions between two people
  - [Webpage](https://computing.ece.vt.edu/~santol/projects/zsl_via_visual_abstraction/index.html)

* [Learning common sense through visual abstraction](AbstractScene/LearningCommonSensethroughVisualAbstraction.pdf) (*ICCV-2015*)
  - **Target**: Assess the plausibility of the interaction in a scene
  - **Dataset**: [Second Generation Abstract Scene Dataset](https://vision.ece.vt.edu/cs/#code_data)
  - [Webpage](https://vision.ece.vt.edu/cs)


## 3D scene generation

#### [Stanford NLP group](https://nlp.stanford.edu/projects/text2scene.shtml)
* [Learning Spatial Knowledge for Text to 3D Scene Generation](3DScene/Text23DSence-LearningSpatialKnowledge.pdf) (*EMNLP-2014*) #thorough
  - **Target**: Text -> 3D scene - room layout
  - **Method**: Mostly rule-based + Bayesian + NLP
  - **Dataset**: [Collected dataset of spatial relation descriptions](http://downloads.cs.stanford.edu/nlp/data/text2scene.shtml#lexground-acl2015)
  - Learned spatial relation mapping

* [Interactive Learning of Spatial Knowledge for Text to 3D Scene Generation
](3DScene/InteractiveLearningofSpatialKnowledgeforTextto3DSceneGeneration.pdf) (*ACL-2014-Workshop*)
  - **Target**: Text -> 3D scene - room layout
  - **Method**: Interactive learning

* [Text to 3D Scene Generation with Rich Lexical Grounding](3DScene/Textto3DSceneGenerationwithRichLexicalGrounding.pdf) (*ACL-2015*) #thorough
  - **Target**: Text -> 3D scene - room layout
  - **Method**: Mostly rule-based + Supervised learning -> learning lexical grounding (i.e. object match)
  - **Dataset**: [Collected dataset of scene-description pairs](http://downloads.cs.stanford.edu/nlp/data/text2scene.shtml#lexground-acl2015)

## 3D shape generation
* [Text2Shape: Generating Shapes from Natural Language by Learning Joint Embeddings](http://text2shape.stanford.edu) (*CVPR-2018*)
  - **Target**: text -> colored 3D shapes of tables and chairs
  - **Method**: Joint metric learning to capture many-to-many relations between text and properties of 3D shapes
  - **Dataset**: [ShapeNet](https://www.shapenet.org) and manually collected text descriptions
  - **Code**: [text2shape](https://github.com/kchen92/text2shape/)

## Photorealistic image synthesis

#### *GAN conditioned on text (Degrade on general images)*

* [Generative Adversarial Text to Image Synthesis](ImageSynthesis/GenerativeAdversarialTexttoImageSynthesis.pdf) (*ICML-2016*)
  - **Target**: text -> photographic image (Bird & flower)
  - **Method**: Both generator and discriminator conditioned on text feature
  - **Dataset**: CUB dataset of bird images; Oxford-102 dataset of flower images
  - **Code**: [Generative Adversarial Text-to-Image Synthesis](https://github.com/reedscot/icml2016)

* [StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks](ImageSynthesis/Zhang_StackGAN_Text_to_ICCV_2017_paper.pdf) (*ICCV-2017*)
  - **Target**: text -> photographic image (Bird & flower)
  - **Method**: two-stage GANs
  - **Dataset**: CUB; Oxford-102; MS-COCO
  - **Code**: [StackGAN](https://github.com/hanzhanggit/StackGAN)

#### *Utilize pixel-wise semantic labels*
* [Parallel multiscale autoregressive density estimation](ImageSynthesis/ParallelMultiscaleAutoregressiveDensityEstimation.pdf) (*ICML-2017*)

#### *Semantic layout as intermediate representation OR Retrieval from oject database*

* [Semi-parametric Image Synthesis](ImageSynthesis/Semi-parametricImageSynthesis.pdf) (*CVPR-2018*)
  - **Target**: Semantic layout -> Photographic image
  - **Method**:
    - Parametric + Non-parametric (segment retrieval)
    - Segment database -> **retrieve** -> composite -> resolve occlusion -> post-process
  - **Dataset**: Cityscapes; NYU; ADE20K (See *Datasets* in this paper)
  - **Code**: [SIMS](https://github.com/xjqicuhk/SIMS)
  - **Demo**: [Semi-parametric Image Synthesis](https://github.com/xjqicuhk/SIMS)

* [Image Generation from Scene Graphs](ImageSynthesis/ImageGenerationfromSceneGraphs.pdf) (*CVPR-2018*)
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

* **[Inferring semantic layout for hierarchical text-to-image synthesis](ImageSynthesis/InferringSemanticLayoutforHierarchicalText-to-ImageSynthesis.pdf)** (*CVPR-2018*)
  - **Target**: text -> photographic image
  - **Method**: text -> **semantic layout (box layout & shape)** -> image
  - **Dataset**: COCO


## Image query

* [Image Ranking and Retrieval based on Multi-Attribute Queries](ImageRankingandRetrievalbasedonMulti-AttributeQueries.pdf) (*CVPR-2011*)

* [Image Retrieval Using Scene Graphs](ImageQuery/ImageRetrievalusingSceneGraphs.pdf) (*CVPR-2015*)
  - **Target**: Textual query -> Semantically related image
  - **Method**: Scene graph; Conditional random field
  - **Dataset**: real-world scene graphs: manually labeled YFCC100m & COCO images

## Video generation
* [Imagine This! Scripts to Compositions to Videos](VideoGeneration/ImageThis_ScriptstoVideos.pdf) (*ECCV-2018*)
  - **Target**: text -> scene video
  - **Method**: Entity & Background retrieval + Layout composer
  - **Dataset**: FLINTSTONES: richly-annotated video-caption dataset
  - **Demo**: [CRAFT](https://youtu.be/688Vv86n0z8)

* [Generating Animated Videos of Human Activities from Natural Language Descriptions](VideoGeneration/GeneratingAnimatedVideosofHumanActivitiesfromNaturalLanguageDescriptions.pdf) (*NIPS-2018*)
  - **Target**: text -> a sequence of 3D human skeletal poses
  - **Method**:
    - **Autoencoder**: Learn a representation of human motions without text
    - Seq2seq: map text into motion representation
  - **Dataset**: [The KIT Motion-Language Dataset](https://motion-annotation.humanoids.kit.edu/dataset/)

* [Language2Pose: Natural Language Grounded Pose Forecasting](https://arxiv.org/abs/1907.01108) (*2019*)
  - **Target**: text -> pose animation
  - **Method**: learn a joint embedding of text and pose using curriculum learning
  - **Dataset**: [The KIT Motion-Language Dataset](https://motion-annotation.humanoids.kit.edu/dataset/)

## Visual story telling
* [A Pipeline for Creative Visual Storytelling](VisualStoryTelling/APipelineforCreativeVisualStorytelling.pdf) (*2018*)
  - **Target**: video -> a sequence of text (Pipeline proposed)

* [Video Storytelling](VisualStoryTelling/VideoStorytelling.pdf) (*2018*)
  - **Target**: video -> a sequence of coherent and succinct text
  - **Method**:
    - Contextual multimodal embedding: Residual Bidirectional RNN
    - Narrator: Reinforcement learning



