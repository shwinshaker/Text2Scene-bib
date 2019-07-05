# Text2Scene-bib
A list of materials related to text2scene

### Rule-Based

#### [Stanford NLP group](https://nlp.stanford.edu/projects/text2scene.shtml)
* [Learning Spatial Knowledge for Text to 3D Scene Generation](Text23DSence-LearningSpatialKnowledge.pdf) (*EMNLP-2014*) #thorough
  - **Style**: Text to 3D scene - room layout
  - **Method**: Mostly rule-based + Bayesian + NLP
  - **Dataset**: [Collected dataset of spatial relation descriptions](http://downloads.cs.stanford.edu/nlp/data/text2scene.shtml#lexground-acl2015)
  - **Code**:
  - Learned spatial relation mapping

* [Text to 3D Scene Generation with Rich Lexical Grounding](Textto3DSceneGenerationwithRichLexicalGrounding.pdf) (*ACL2015*) #thorough
  - **Style**: Text to 3D scene - room layout
  - **Method**: Mostly rule-based
  - **Dataset**: [Collected dataset of scene-description pairs](http://downloads.cs.stanford.edu/nlp/data/text2scene.shtml#lexground-acl2015)
  - **Code**:
  - Learned lexical grounding (object)

* [Interactive Learning of Spatial Knowledge for Text to 3D Scene Generation
](InteractiveLearningofSpatialKnowledgeforTextto3DSceneGeneration.pdf) (*ACL2014-Workshop*)
  - Text to 3D scene - room layout
  - Mostly rule-based
  - Interactive learning

### GAN

### GAN-free
* [Learning the Visual Interpretation of Sentences](LearningVisualInterpretationofSentences.pdf)
  - Text to 2D scene
  - Cartoon-like
  - Statistical: Conditional Random Field (CRF)
  - Public dataset: [Abstract Scene Dataset](https://vision.ece.vt.edu/clipart/)

* **[Text2Scene: Generating Compositional Scenes from Textual Descriptions](Text2Scene.pdf)** #thorough
  - **Style**: Text to 2D scene; Cartoon-like & Sythesis
  - **Method**: End2end deep learning (Recurrent CNN + attention); Unified framework
  - **Dataset**: [Abstract Scene Dataset](https://vision.ece.vt.edu/clipart/); COCO
  - **Code**: [Text2Scene](https://github.com/uvavision/Text2Scene)
  
