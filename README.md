# Forked From: 
https://github.com/fuzhenxin/Style-Transfer-in-Text
Zhenxin Fu (fuzhenxin95@gmail.com) from Peking University.  

- Commments Contributed by **[Jingyun Xu]**, from 2016-, 2020.4.29.
- :whale2: 取自静云(鲸鱼), :whale2: 的数量仅表示个人喜好的程度 :kissing_heart:, :heart_eyes: 表示想去细读的, :dizzy_face:表示看了，没有完全看懂的。

# A Paper List for Style Transfer in Text
This is a paper list for style transfer in text. It also contains some related research areas, including controlled text generation.

**Keyword:** *Style Transfer, Unsupervised, Natural Language Processing*

# Paper List
## Dataset
- Dear Sir or Madam, May I introduce the YAFC Corpus: Corpus, Benchmarks and Metrics for Formality Style Transfer, NAACL-HLT 2018, [[paper]](https://arxiv.org/abs/1803.06535)
- A Dataset for Low-Resource Stylized Sequence-to-Sequence Generation, AAAI, 2020, [[paper]](https://www.msra.cn/wp-content/uploads/2020/01/A-Dataset-for-Low-Resource-Stylized-Sequence-to-Sequence-Generation.pdf), [[code]](https://github.com/MarkWuNLP/Data4StylizedS2S)
- Evaluating Neural Text Simplification in the Medical Domain, WWW, 2019, [[paper]](https://pdfs.semanticscholar.org/093c/f4ede717d69d6e1e6763a3f7b4ad3ed3f3bd.pdf)

## Supervised (Parallel Data)
- Shakespearizing Modern Language Using Copy-Enriched Sequence to Sequence Models, EMNLP-2017 Workshop, [[paper]](https://arxiv.org/abs/1707.01161)[[code]](https://github.com/harsh19/Shakespearizing-Modern-English)
- Evaluating prose style transfer with the Bible, 2018, [[paper]](https://arxiv.org/abs/1711.04731)
- Harnessing Pre-Trained Neural Networks with Rules for Formality Style Transfer, EMNLP-2019, [[paper]](https://www.aclweb.org/anthology/D19-1365/), [[code]](https://github.com/jimth001/formality_emnlp19)

## Unsupervised (Non-parallel Data)
### 基于GAN的模型 Style和Content隐式分开
- Utilizing Non-Parallel Text for Style Transfer by Making Partial Comparisonsn, IJCAI-2019, [[paper]](https://www.ijcai.org/Proceedings/2019/0747.pdf), [[code]](https://github.com/yd1996/awesome-text-style-transfer) [:whale2::whale2::whale2::whale2::whale2:] 
```   
Motivation:   
目前基于GAN的文本风格迁移模型的面临的挑战:
1. 生成的新text在保留原先的content方面仍有待提高

Model:
图片左边是原先的模型,直接判别生成的内容是否改变了style,而右边的模型则将判别器分为2部分,1部分判别生成的content是否保留,另一部分则判别style是否改变。
```
Model:
![](https://github.com/LittleSummer114/Style-Transfer-in-Text/blob/master/IJCAI%202019.PNG)

### 基于encoder-decoder的模型 Style和Content隐式分开
- Style Transfer in Text: Exploration and Evaluation, AAAI-2018, [[paper]](https://arxiv.org/abs/1711.06861), [[code]](https://github.com/fuzhenxin/text_style_transfer)
```   
Motivation:   
目前文本风格迁移领域的面临的挑战:
1. 缺乏并行语料
2. 缺乏可靠的评价方法

针对缺乏并行语料的情况,作者提出了2个基于非并行语料的模型,1个模型是基于multi-decoder,encoder编码输入的content,decoder针对相同的content输出不同style的表达,另1个模型也是基于相同的encoder,decoder只有1个,引入了style embeddings来编码style.

针对缺乏可靠的评价方法的情况,作者提出了2个评价方法,分别验证了文本风格迁移的2个方面:内容的保留情况和迁移的强度。

Contributions:
1. 提出了1个paper-new方面的数据集
2. 提出了2个模型
3. 提出了2个评价方法

Question List:    
1. 如何做的？如何处理缺乏Non-Parallel语料的问题?
```
![](https://github.com/LittleSummer114/Natural-Language-Inference-Paper-List/blob/master/images/Visual-1.PNG)

- Sequence to Better Sequence: Continuous Revision of Combinatorial Structures, ICML-2017, [[paper]](http://proceedings.mlr.press/v70/mueller17a.html), [[code]](https://bitbucket.org/jwmueller/sequence-to-better-sequence/)


- Toward Controlled Generation of Text, ICML-2017, [[paper]](https://arxiv.org/abs/1703.00955), [[official code]](https://github.com/asyml/texar/tree/master/examples/text_style_transfer), [[unofficial code]](https://github.com/GBLin5566/toward-controlled-generation-of-text-pytorch)
- Style Transfer from Non-Parallel Text by Cross-Alignment, NIPS-2017, [[paper]](https://papers.nips.cc/paper/7259-style-transfer-from-non-parallel-text-by-cross-alignment.pdf), [[code]](https://github.com/shentianxiao/language-style-transfer)
- Adversarially Regularized Autoencoders, ICML-2018, [[paper]](https://arxiv.org/abs/1706.04223), [[code]](https://github.com/jakezhaojb/ARAE)
- Zero-Shot Style Transfer in Text Using Recurrent Neural Networks, Arxiv-2017, [[paper]](https://arxiv.org/abs/1711.04731), [[code]](https://github.com/keithecarlson/Zero-Shot-Style-Transfer)
- Delete, Retrieve, Generate: A Simple Approach to Sentiment and Style Transfer, NAACL-2018, [[paper]](https://arxiv.org/abs/1804.06437), [[code]](https://worksheets.codalab.org/worksheets/0xe3eb416773ed4883bb737662b31b4948/)
- SHAPED: Shared-Private Encoder-Decoder for Text Style Adaptation, NAACL-2018, [[paper]](https://arxiv.org/abs/1804.04093)
- Sentiment Transfer using Seq2Seq Adversarial Autoencoders, project for CSYE7245 Northeastern University, [[paper]](https://arxiv.org/abs/1804.04003)
- Style Transfer Through Back-Translation, ACL-2018, [[paper]](https://arxiv.org/abs/1804.09000), [[code]](https://github.com/shrimai/Style-Transfer-Through-Back-Translation)
- Unpaired Sentiment-to-Sentiment Translation: A Cycled Reinforcement Learning Approach, ACL-2018, [[paper]](https://arxiv.org/abs/1805.05181), [[code]](https://github.com/lancopku/unpaired-sentiment-translation)
- Fighting Offensive Language on Social Media with Unsupervised Text Style Transfer, ACL-2018, [[paper]](https://arxiv.org/abs/1805.07685)
- Unsupervised Text Style Transfer using Language Models as Discriminators, NIPS-2018, [[paper]](https://arxiv.org/abs/1805.11749)
- Disentangled Representation Learning for Text Style Transfer, Arxiv, [[paper]](https://arxiv.org/abs/1808.04339), [[code]](https://github.com/vineetjohn/linguistic-style-transfer)
- Language Style Transfer from Sentences with Arbitrary Unknown Styles, Arxiv, [[paper]](https://arxiv.org/abs/1808.04071)
- What is wrong with style transfer for texts? Arxiv, [[paper]](https://arxiv.org/abs/1808.04365)
- Style Transfer as Unsupervised Machine Translation, Arxiv, [[paper]](https://arxiv.org/abs/1808.07894)
- Learning Sentiment Memories for Sentiment Modification without Parallel Data, EMNLP-2018, [[paper]](https://arxiv.org/abs/1808.07311), [[code]](https://github.com/lancopku/SMAE)
- Style Transfer Through Multilingual and Feedback-Based Back-Translation, Arxiv, 2018, [[paper]](https://arxiv.org/abs/1809.06284)
- Structured Content Preservation for Unsupervised Text Style Transfer, OpenReview, 2018, [[paper]](https://openreview.net/forum?id=S1lCbhAqKX)
- Unsupervised Controllable Text Formalization, AAAI, 2019, [[paper]](https://arxiv.org/abs/1809.04556), [[code]](https://github.com/parajain/uctf)
- Large-scale Hierarchical Alignment for Data-driven Text Rewriting, RANLP, 2019, [[paper]](https://arxiv.org/abs/1810.08237)
- Learning Criteria and Evaluation Metrics for Textual Transfer between Non-Parallel Corpora, Arxiv, 2018, [[paper]](https://arxiv.org/abs/1810.11878)
- Content preserving text generation with attribute controls, NIPS, 2018, [[paper]](https://arxiv.org/abs/1811.01135)
- QuaSE: Sequence Editing under Quantifiable Guidance, EMNLP, 2018, [[paper]](http://aclweb.org/anthology/D18-1420)
- Adversarial Text Generation via Feature-Mover's Distance, NeurIPS, 2018, [[paper]](https://arxiv.org/abs/1809.06297), [[unofficial code]](https://github.com/knok/chainer-fm-gan)
- Towards Controlled Transformation of Sentiment in Sentences, ICAART, 2019, [[paper]](https://arxiv.org/abs/1901.11467)
- Formality Style Transfer with Hybrid Textual Annotations, Arxiv, 2019, [[paper]](https://arxiv.org/abs/1903.06353)
- Reinforcement Learning Based Text Style Transfer without Parallel Training Corpus, NAACL-2019, 2019, [[paper]](https://arxiv.org/abs/1903.10671)
- Grammatical Error Correction and Style Transfer via Zero-shot Monolingual Translation, Arxiv, 2019, [[paper]](https://arxiv.org/abs/1903.11283)
- Multiple-Attribute Text Style Transfer (Rewriting), ICLR, 2019, [[paper]](https://openreview.net/forum?id=H1g2NhC5KQ)
- Style Transformer: Unpaired Text Style Transfer without Disentangled Latent Representation, ACL, 2019, [[paper]](https://arxiv.org/abs/1905.05621)
- A Dual Reinforcement Learning Framework for Unsupervised Text Style Transfer, IJCAI, 2019, [[paper]](https://arxiv.org/abs/1905.10060), [[code]](https://github.com/luofuli/DualLanST)
- On Variational Learning of Controllable Representations for Text without Supervision, Arxiv, 2019, [[paper]](https://arxiv.org/abs/1905.11975)
- Revision in Continuous Space: Fine-Grained Control of Text Style Transfer, AAAI, 2020, [[paper]](https://arxiv.org/abs/1905.12304)
- Controllable Unsupervised Text Attribute Transfer via Editing Entangled Latent Representation, NIPS, 2019, [[paper]](https://arxiv.org/abs/1905.12926), [[code]](https://github.com/nrgeup/controllable-text-attribute-transfer)
- Disentangled Representation Learning for Non-Parallel Text Style Transfer, ACL, 2019, [[paper]](https://www.aclweb.org/anthology/P19-1041), [[code]](https://github.com/vineetjohn/linguistic-style-transfer)
- A Hierarchical Reinforced Sequence Operation Method for Unsupervised Text Style Transfer, ACL, 2019, [[paper]](https://www.aclweb.org/anthology/P19-1482), [[code]](https://github.com/ChenWu98/Point-Then-Operate)
- Unsupervised Text Attribute Transfer via Iterative Matching and Translation, EMNLP, 2019, [[paper]](https://arxiv.org/abs/1901.11333)
- Mask and Infill: Applying Masked Language Model to Sentiment Transfer, IJCAI, 2019, [[paper]](https://arxiv.org/abs/1908.08039)
- Transforming Delete, Retrieve, Generate Approach for Controlled Text Style Transfer, EMNLP, 2019, [[paper]](https://arxiv.org/abs/1908.09368), [[code]](https://github.com/agaralabs/transformer-drg-style-transfer)
- Domain Adaptive Text Style Transfer, EMNLP, 2019, [[paper]](https://arxiv.org/abs/1908.09395), [[code]](https://github.com/cookielee77/DAST)
- Style Transfer for Texts: Retrain, Report Errors, Compare with Rewrites, EMNLP, 2019, [[paper]](https://arxiv.org/pdf/1908.06809.pdf), [[code]](https://github.com/VAShibaev/text_style_transfer)
- Decomposing Textual Information For Style Transfer, WNGT, 2019, [[paper]](https://arxiv.org/abs/1909.12928)
- Zero-Shot Fine-Grained Style Transfer: Leveraging Distributed Continuous Style Representations to Transfer To Unseen Styles, Arxiv, 2019, [[paper]](https://arxiv.org/abs/1911.03914)
- A Probabilistic Formulation of Unsupervised Text Style Transfer, ICLR, 2020, [[paper]](https://openreview.net/forum?id=HJlA0C4tPS), [[code]](https://github.com/cindyxinyiwang/deep-latent-sequence-model)
- Generating sentences from disentangled syntactic and semantic spaces, ACL, 2019, [[paper]](https://www.aclweb.org/anthology/P19-1602/)
- SentiInc: Incorporating Sentiment Information into Sentiment Transfer Without Parallel Data, ECIR, 2020, [[paper]](https://link.springer.com/content/pdf/10.1007%2F978-3-030-45442-5_39.pdf)

# Semi-supervised
- Semi-supervised Text Style Transfer: Cross Projection in Latent Space, EMNLP, 2019, [[paper]](https://arxiv.org/abs/1909.11493)

## Evaluation and Analysis
- Evaluating Style Transfer for Text, NAACL, 2019, [[paper1]](https://arxiv.org/abs/1904.02295), [[paper2]](https://dspace.mit.edu/bitstream/handle/1721.1/119569/1076275047-MIT.pdf?sequence=1)
- Rethinking Text Attribute Transfer: A Lexical Analysis, INLG, 2019, [[paper]](https://arxiv.org/abs/1909.12335), [[code]](https://github.com/FranxYao/pivot_analysis)
- Unsupervised Evaluation Metrics and Learning Criteria for Non-Parallel Textual Transfer, EMNLP Workshop on Neural Generation and Translation (WNGT), 2019, [[paper]](https://arxiv.org/abs/1810.11878)
- The Daunting Task of Real-World Textual Style Transfer Auto-Evaluation, WNGT, 2019, [[paper]](https://arxiv.org/abs/1910.03747)
- Style-transfer and Paraphrase: Looking for a Sensible Semantic Similarity Metric, Arxiv, 2020, [[paper]](https://arxiv.org/pdf/2004.05001.pdf)

## Stylistic Related Papers
- Controlling Linguistic Style Aspects in Neural Language Generation, EMNLP-2017 Workshop, [[paper]](https://arxiv.org/abs/1707.02633)
- Is writing style predictive of scientific fraud?, EMNLP-2017 Workshop, [[paper]](http://www.aclweb.org/anthology/W17-4905)
- Incorporating Pseudo-Parallel Data for Quantifiable Sequence Editing, EMNLP-2018, [[paper]](https://arxiv.org/abs/1804.07007)
- Polite Dialogue Generation Without Parallel Data, TACL, [[paper]](https://arxiv.org/abs/1805.03162)
- Adversarial Decomposition of Text Representation, Arxiv, [[paper]](https://arxiv.org/abs/1808.09042)
- Unsupervised Stylish Image Description Generation via Domain Layer Norm, AAAI 2019, [[paper]](https://arxiv.org/abs/1809.06214)
- Transfer Learning for Style-Specific Text Generation, UNK, 2018, [[paper]](https://nips2018creativity.github.io/doc/Transfer%20Learning%20for%20Style-Specific%20Text%20Generation.pdf)
- Generating lyrics with variational autoencoder and multi-modal artist embeddings, Arxiv, 2018, [[paper]](https://arxiv.org/abs/1812.08318)
- Generating Sentences by Editing Prototypes, TACL, 2018, [[paper]](https://www.aclweb.org/anthology/Q18-1031/)
- ALTER: Auxiliary Text Rewriting Tool for Natural Language Generation, EMNLP, 2019, [[paper]](https://arxiv.org/abs/1909.06564)
- Stylized Text Generation Using Wasserstein Autoencoders with a Mixture of Gaussian Prior, Arxiv, 2019, [[paper]](https://arxiv.org/abs/1911.03828)
- Adapting Language Models for Non-Parallel Author-Stylized Rewriting, AAAI, 2020 [[paper]](https://arxiv.org/abs/1909.09962)
- Structuring Latent Spaces for Stylized Response Generation, EMNLP, 2019, [[paper]](https://arxiv.org/abs/1909.05361)
- Complementary Auxiliary Classifiers for Label-Conditional Text Generation, AAAI, 2020, [[paper]](http://people.ee.duke.edu/~lcarin/AAAI_LiY_6828.pdf), [[code]](https://github.com/s1155026040/CARA)

# Workshop
- Stylistic Variation, EMNLP-2017, [[link]](https://sites.google.com/site/workshoponstylisticvariation/)
- Stylistic Variation, NAACL-HLT-2018, [[link]](https://sites.google.com/view/2ndstylisticvariation/home)
