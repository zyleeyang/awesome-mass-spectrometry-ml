# Awesome Deep Learning Methods in Analytical Chemistry

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Keep updating the deep learning papers and codes related to analytical chemistry. Contributes are always welcome!

```markdown
1. Papers without any implementation codes are excluded from this list. 

2. Format: 
    - [conference/journal name year] [(optional) model name] <MLA cite> [[paper]]() [[code]]() 
```



## Contents

* [Small molecular representation](#small_molecular_representation)
    * [Point-based (or quantum-based) methods](#point-based-or-quantum-based-methods)
    * [Graph-based methods](#graph-based-methods)
    * [Sequence-based methods](#sequence-based-methods)
* [Analytical chemistry-related properties prediction](#analytical_chem_prediction)
* [Small molecular generation](#small_molecular_generation)
* [Small molecular optimization](#small_molecular_optimization)



## Small molecular representation learning <a id="small_molecular_representation_learning"></a>

The molecular representation learning or properties prediction models are categorized as point-based (or quantum-based) methods, graph-based methods, and sequence-based methods. Because the number of graph-based methods is huge, they are further divided into self-supervised learning and supervised learning manners. It is worth noting that the difference between point-based (or quantum-based) methods and graph-based methods is if bonds (i.e. edges) are included in the encoding. 

|                                | # Paper | Note                       |
|--------------------------------|---------|----------------------------|
| Point-Based (or Quantum-Based) | 2       | 3D, No bonds are encoded   |
| Graph-Based                    | 20      | 2D & 3D, Bonds are encoded |
| Sequence-Based                 | 1       | 1D                         |

### Point-based (or quantum-based) methods

- [ICLR 2023] Zhou, Gengmo, et al. "Uni-mol: A universal 3d molecular representation learning framework." (2023). [[paper]](https://chemrxiv.org/engage/chemrxiv/article-details/6402990d37e01856dc1d1581) [[code]](https://github.com/dptech-corp/Uni-Mol)
- [PMLR 2021] [PaiNN] Schütt, Kristof, Oliver Unke, and Michael Gastegger. "Equivariant message passing for the prediction of tensorial properties and molecular spectra." International Conference on Machine Learning. PMLR, 2021. [[paper]](https://proceedings.mlr.press/v139/schutt21a.html?ref=https://githubhelp.com) [[code]](https://github.com/atomistic-machine-learning/schnetpack)
- [NeurIPS 2017] [SchNet] Schütt, Kristof, et al. "Schnet: A continuous-filter convolutional neural network for modeling quantum interactions." Advances in neural information processing systems 30 (2017). [[paper]](https://proceedings.neurips.cc/paper/2017/hash/303ed4c69846ab36c2904d3ba8573050-Abstract.html) [[code]](https://github.com/atomistic-machine-learning/SchNet)

### Graph-based methods

Because there are lots of graph-based models, we categorize them into supervised learning methods and self-supervised methods. 

**Self-Supervised Learning**

- [Bioinformatics 2023] [3DGCL] Moon, Kisung, Hyeon-Jin Im, and Sunyoung Kwon. "3D graph contrastive learning for molecular property prediction." Bioinformatics 39.6 (2023): btad371. [[paper]](https://academic.oup.com/bioinformatics/article/39/6/btad371/7192173) [[code]](https://github.com/moonkisung/3DGCL)
- [ICLR 2023] [Mole-BERT] Xia, Jun, et al. "Mole-bert: Rethinking pre-training graph neural networks for molecules." The Eleventh International Conference on Learning Representations. 2022. [[paper]](https://openreview.net/forum?id=jevY-DtiZTR) [[code]](https://github.com/junxia97/Mole-BERT/tree/2feff8a33e3634b66b7408e2e2780fc9d960909f)
- [ICLR 2023 (spotlight)] [GNS TAT] Zaidi, Sheheryar, et al. "Pre-training via denoising for molecular property prediction." arXiv preprint arXiv:2206.00133 (2022). [[paper]](https://arxiv.org/abs/2206.00133) [[code]](https://github.com/shehzaidi/pre-training-via-denoising) 
- [ICLR 2023] [GeoSSL-DDM] Liu, Shengchao, Hongyu Guo, and Jian Tang. "Molecular geometry pretraining with se (3)-invariant denoising distance matching." arXiv preprint arXiv:2206.13602 (2022). [[paper]](https://arxiv.org/abs/2206.13602) [[code]](https://github.com/chao1224/GeoSSL) 
- [ICLR 2022] [GraphMVP] Liu, Shengchao, et al. "Pre-training molecular graph representation with 3d geometry." arXiv preprint arXiv:2110.07728 (2021). [[paper]](https://arxiv.org/abs/2110.07728) [[code]](https://github.com/chao1224/GraphMVP) 
- [NeurIPS 2021] [MGSSL] Zhang, Zaixi, et al. "Motif-based graph self-supervised learning for molecular property prediction." Advances in Neural Information Processing Systems 34 (2021): 15870-15882. [[paper]](https://arxiv.org/abs/2110.00987) [[code]](https://github.com/zaixizhang/MGSSL) 
- [NeurIPS 2020] [GROVER] Rong, Yu, et al. "Self-supervised graph transformer on large-scale molecular data." Advances in Neural Information Processing Systems 33 (2020): 12559-12571. [[paper]](https://proceedings.neurips.cc/paper/2020/hash/94aef38441efa3380a3bed3faf1f9d5d-Abstract.html) [[code]](https://github.com/tencent-ailab/grover)
- [ICLR 2020] [InfoGraph] Sun, Fan-Yun, et al. "Infograph: Unsupervised and semi-supervised graph-level representation learning via mutual information maximization." arXiv preprint arXiv:1908.01000 (2019). [[paper]](https://arxiv.org/abs/1908.01000) [[code]](https://github.com/sunfanyunn/InfoGraph) 

**Supervised Learning**

- [AAAI 2023] [Molformer] Wu, Fang, Dragomir Radev, and Stan Z. Li. "Molformer: Motif-based transformer on 3d heterogeneous molecular graphs." Proceedings of the AAAI Conference on Artificial Intelligence. Vol. 37. No. 4. 2023. [[paper]](https://ojs.aaai.org/index.php/AAAI/article/view/25662) [[code]](https://github.com/smiles724/Molformer/tree/master)
- [NeurIPS 2022] [ComENet] Wang, Limei, et al. "ComENet: Towards Complete and Efficient Message Passing for 3D Molecular Graphs." arXiv preprint arXiv:2206.08515 (2022). [[paper]](https://openreview.net/forum?id=mCzMqeWSFJ) [[code (implemented in DIG library)]](https://github.com/divelab/DIG/blob/b54e27e5660f0a8ba31dbc7d3f056f872b1f3e8e/dig/threedgraph/method/comenet/ocp/README.md) 
- [ICLR 2022] [GNS+Noisy Nodes] Godwin, Jonathan, et al. "Simple GNN regularisation for 3D molecular property prediction & beyond." arXiv preprint arXiv:2106.07971 (2021). [[paper]](https://arxiv.org/abs/2106.07971) [[codes]](https://github.com/Namkyeong/NoisyNodes_Pytorch)
- [ICLR 2022] [MolR] Wang, Hongwei, et al. "Chemical-reaction-aware molecule representation learning." arXiv preprint arXiv:2109.09888 (2021). [[paper]](https://arxiv.org/abs/2109.09888) [[code]](https://github.com/hwwang55/MolR) 
- [ICLR 2022] [SphereNet] Liu, Yi, et al. "Spherical message passing for 3d graph networks." arXiv preprint arXiv:2102.05013 (2021). [[paper]](https://arxiv.org/abs/2102.05013) [[code (implemented in DIG library)]](https://github.com/divelab/DIG) 
- [Nat. Mach. Intell. 2022] [GEM] Fang, Xiaomin, et al. "Geometry-enhanced molecular representation learning for property prediction." Nature Machine Intelligence 4.2 (2022): 127-134. [[paper]](https://www.nature.com/articles/s42256-021-00438-4.) [[code]](https://github.com/PaddlePaddle/PaddleHelix/tree/dev/apps/pretrained_compound/ChemRL/GEM) 
- [Brief. Bioinformatics 2021] [TrimNet] Li, Pengyong, et al. "TrimNet: learning molecular representation from triplet messages for biomedicine." Briefings in Bioinformatics 22.4 (2021): bbaa266. [[paper]](https://academic.oup.com/bib/article-abstract/22/4/bbaa266/5955940) [[code]](https://github.com/yvquanli/TrimNet)
- [NeurIPS 2021] [GemNet] Gasteiger, Johannes, Florian Becker, and Stephan Günnemann. "Gemnet: Universal directional graph neural networks for molecules." Advances in Neural Information Processing Systems 34 (2021): 6790-6802. [[paper]](https://proceedings.neurips.cc/paper/2021/hash/35cf8659cfcb13224cbd47863a34fc58-Abstract.html) [[code]](https://github.com/TUM-DAML/gemnet_pytorch)
- [NeurIPS 2020] [DimeNet++] Klicpera, Johannes, et al. "Fast and uncertainty-aware directional message passing for non-equilibrium molecules." arXiv preprint arXiv:2011.14115 (2020). [[paper]](https://arxiv.org/abs/2011.14115) [[code]](https://github.com/gasteigerjo/dimenet)
- [ICLR 2020] [DimeNet] Gasteiger, Johannes, Janek Groß, and Stephan Günnemann. "Directional message passing for molecular graphs." arXiv preprint arXiv:2003.03123 (2020). [[paper]](https://arxiv.org/abs/2003.03123) [[code]](https://github.com/gasteigerjo/dimenet)
- [Chem. Mater 2019] [MEGNet] Chen, Chi, et al. "Graph networks as a universal machine learning framework for molecules and crystals." Chemistry of Materials 31.9 (2019): 3564-3572. [[paper]](https://pubs.acs.org/doi/full/10.1021/acs.chemmater.9b01294?casa_token=Qt91hGc97ywAAAAA%3A_uRAvtFkZVg-YHOeSw1mgP5K-pHBPqUpErJFugRveatjcHKJzcsoQACGsBbIxXJ0CFrY2Ug2jnXgcA) [[preprint]](https://arxiv.org/abs/1812.05055) [[code]](https://github.com/materialsvirtuallab/megnet)
- [PMLR 2017] Gilmer, Justin, et al. "Neural message passing for quantum chemistry." International conference on machine learning. PMLR, 2017. [[paper]](https://proceedings.mlr.press/v70/gilmer17a) [[code]](https://github.com/brain-research/mpnn) 
- [NeurIPS 2015] [Neural Graph Fingerprints] Duvenaud, David K., et al. "Convolutional networks on graphs for learning molecular fingerprints." Advances in neural information processing systems 28 (2015). [[paper]](https://proceedings.neurips.cc/paper/2015/hash/f9be311e65d81a9ad8150a60844bb94c-Abstract.html) [[code]](https://github.com/HIPS/neural-fingerprint)

**Other Related Works**

- [NeurIPS 2020] You, Yuning, et al. "Graph contrastive learning with augmentations." Advances in neural information processing systems 33 (2020): 5812-5823. [[paper]](https://proceedings.neurips.cc/paper/2020/hash/3fe230348e9a12c13120749e3f9fa4cd-Abstract.html) [[code]](https://github.com/Shen-Lab/GraphCL) 
- [ICLR 2020] Hu, Weihua, et al. "Strategies for pre-training graph neural networks." arXiv preprint arXiv:1905.12265 (2019). [[paper]](https://arxiv.org/abs/1905.12265) [[code]](https://github.com/snap-stanford/pretrain-gnns/) 


### Sequence-based methods

- [BCB 2019] [SMILES-BERT] Wang, Sheng, et al. "SMILES-BERT: large scale unsupervised pre-training for molecular property prediction." Proceedings of the 10th ACM international conference on bioinformatics, computational biology and health informatics. 2019. [[paper]](https://dl.acm.org/doi/abs/10.1145/3307339.3342186?casa_token=ROSIBxMX2UkAAAAA:q9M-DLpNJozQWqWEABwskuANeWuj8dPhU9ijopTfmnXJw3l7bjUuKEXI-br4yc4PG5cxVU5MT5Y) [[code]](https://github.com/uta-smile/SMILES-BERT)



## Analytical chemistry-related properties prediction <a id="analytical_chem_prediction"></a>

**MS/MS predicton**

- [Nat. Mach. Intell. 2023] Goldman, Samuel, et al. "Annotating metabolite mass spectra with domain-inspired chemical formula transformers." Nature Machine Intelligence 5.9 (2023): 965-979. [[paper]](https://www.nature.com/articles/s42256-023-00708-3) [[code]](https://github.com/samgoldman97/mist)
- [arxiv 2023] Young, Adamo, Bo Wang, and Hannes Röst. "MassFormer: Tandem mass spectrum prediction with graph transformers." arXiv preprint arXiv:2111.04824 (2021). [[paper]](https://arxiv.org/abs/2111.04824) [[code]](https://github.com/Roestlab/massformer)
- [NeurIPS 2023] Goldman, Samuel, et al. "Prefix-tree decoding for predicting mass spectra from molecules." arXiv preprint arXiv:2303.06470 (2023). [[paper]](https://arxiv.org/abs/2303.06470) [[code]](https://github.com/samgoldman97/ms-pred)
- [Bioinformatics 2023] Hong, Yuhui, et al. "3DMolMS: prediction of tandem mass spectra from 3D molecular conformations." Bioinformatics 39.6 (2023): btad354. [[paper]](https://academic.oup.com/bioinformatics/article/39/6/btad354/7186501) [[code]](https://github.com/JosieHong/3DMolMS)
- [Anal. Chem. 2021] Wang, Fei, et al. "CFM-ID 4.0: more accurate ESI-MS/MS spectral prediction and compound identification." Analytical chemistry 93.34 (2021): 11692-11700. [[paper]](https://pubs.acs.org/doi/full/10.1021/acs.analchem.1c01465) [[code]](https://hub.docker.com/r/wishartlab/cfmid)
- [ACS Cent. Sci. 2019] Wei, Jennifer N., et al. "Rapid prediction of electron–ionization mass spectrometry using neural networks." ACS central science 5.4 (2019): 700-708. [[paper]](https://pubs.acs.org/doi/full/10.1021/acscentsci.9b00085) [[code]](https://github.com/brain-research/deep-molecular-massspec)

**Retetntion time prediction**



**Collision cross section prediction**



## Small molecular generation <a id="small_molecular_generation"></a>

Based on the training strategies, deep molecular generative models can be classified into two categories: reinforcement learning (RL)-based methods, which generate molecules with desired properties; unsupervised (UL)-based or self-supervised (SSL)-based methods, which aim to generate valid, novel, and diverse molecules; supervised (SL)-based methods generating molecular three-dimensional conformations from molecular graphs. 

|                                                         | # paper  |
|---------------------------------------------------------|----------|
| RL-Based Generator                                      | 2        |
| SL-Based Generator - Molecular Conformation             | 10       |
| UL-Based & SSL-Based Generator - Molecular Graph        | 11       |
| UL-Based & SSL-Based Generator - SMILES String          | 6        |

**RL-based generators**

- [NeurIPS 2018] [GCPN] You, Jiaxuan, et al. "Graph convolutional policy network for goal-directed molecular graph generation." Advances in neural information processing systems 31 (2018). [[paper]](https://proceedings.neurips.cc/paper/2018/hash/d60678e8f2ba9c540798ebbde31177e8-Abstract.html) [[code]](https://github.com/bowenliu16/rl_graph_generation) 
- [Sci. Adv. 2018] [ReLeaSE] Popova, Mariya, Olexandr Isayev, and Alexander Tropsha. "Deep reinforcement learning for de novo drug design." Science advances 4.7 (2018): eaap7885. [[paper]](https://www.science.org/doi/10.1126/sciadv.aap7885) [[code]](https://github.com/isayev/ReLeaSE)

**SL-based generator - molecular conformation**

- [ICLR 2022 (Oral)] [GeoDiff] Xu, Minkai, et al. "Geodiff: A geometric diffusion model for molecular conformation generation." arXiv preprint arXiv:2203.02923 (2022). [[paper]](https://openreview.net/forum?id=PzcvxEMzvQC) [[code]](https://github.com/MinkaiXu/GeoDiff) 
- [NeurIPS 2022] [torsional diffusion] Jing, Bowen, et al. "Torsional diffusion for molecular conformer generation." arXiv preprint arXiv:2206.01729 (2022). [[paper]](https://arxiv.org/abs/2206.01729) [[code]](https://github.com/gcorso/torsional-diffusion) 
- [TMLR 2022] [DMCG] Zhu, Jinhua, et al. "Direct molecular conformation generation." arXiv preprint arXiv:2202.01356 (2022). [[paper]](https://arxiv.org/abs/2202.01356) [[code]](https://github.com/DirectMolecularConfGen/DMCG) 
- [NeurIPS 2021] [GeoMol] Ganea, Octavian, et al. "Geomol: Torsional geometric generation of molecular 3d conformer ensembles." Advances in Neural Information Processing Systems 34 (2021): 13757-13769. [[paper]](https://proceedings.neurips.cc/paper/2021/hash/725215ed82ab6306919b485b81ff9615-Abstract.html) [[code]](https://github.com/PattanaikL/GeoMol)
- [NeurIPS 2021] [DGSM] Luo, Shitong, et al. "Predicting molecular conformation via dynamic graph score matching." Advances in Neural Information Processing Systems 34 (2021): 19784-19795. [[paper]](https://proceedings.neurips.cc/paper/2021/hash/a45a1d12ee0fb7f1f872ab91da18f899-Abstract.html) 😢 No official codes are available.
- [ICML 2021] [ConfGF] Shi, Chence, et al. "Learning gradient fields for molecular conformation generation." International Conference on Machine Learning. PMLR, 2021. [[paper]](http://proceedings.mlr.press/v139/shi21b.html) [[code]](https://github.com/DeepGraphLearning/ConfGF) 
- [ICML 2021] [ConfVAE] Xu, Minkai, et al. "An end-to-end framework for molecular conformation generation via bilevel programming." International Conference on Machine Learning. PMLR, 2021. [[paper]](http://proceedings.mlr.press/v139/xu21f.html) [[code]](https://github.com/MinkaiXu/ConfVAE-ICML21) 
- [ICLR 2021] [CGCF] Xu, Minkai, et al. "Learning neural generative dynamics for molecular conformation generation." arXiv preprint arXiv:2102.10240 (2021). [[paper]](https://arxiv.org/abs/2102.10240) [[code]](https://github.com/DeepGraphLearning/CGCF-ConfGen) 
- [NeurIPS 2020] [TorsionNet] Gogineni, Tarun, et al. "Torsionnet: A reinforcement learning approach to sequential conformer search." Advances in Neural Information Processing Systems 33 (2020): 20142-20153. [[paper]](https://proceedings.neurips.cc/paper/2020/hash/e904831f48e729f9ad8355a894334700-Abstract.html) [[code]](https://github.com/tarungog/torsionnet_paper_version) 
- [ICML 2020] [GraphDG] Simm, Gregor NC, and José Miguel Hernández-Lobato. "A generative model for molecular distance geometry." arXiv preprint arXiv:1909.11459 (2019). [[paper]](https://arxiv.org/abs/1909.11459) [[code]](https://github.com/gncs/graphdg) 
- [Sci. Rep. 2019] [CVGAE] Mansimov, Elman, et al. "Molecular geometry prediction using a deep generative graph neural network." Scientific reports 9.1 (2019): 20381. [[paper]](https://www.nature.com/articles/s41598-019-56773-5) [[code]](https://github.com/nyu-dl/dl4chem-geometry) 

**UL-based & SSL-based generator - molecular graph**

- [ICLR 2022 (Oral)] [DEG] Guo, Minghao, et al. "Data-efficient graph grammar learning for molecular generation." arXiv preprint arXiv:2203.08031 (2022). [[paper]](https://openreview.net/forum?id=l4IHywGq6a) [[code]](https://github.com/gmh14/data_efficient_grammar) 
- [ICLR 2022 (Spotlight)] [STGG] Ahn, Sungsoo, et al. "Spanning tree-based graph generation for molecules." International Conference on Learning Representations. 2021. [[paper]](https://openreview.net/forum?id=w60btE_8T2m) 😢 No official codes are available. 
- [ICML 2021] [GraphDF] Luo, Youzhi, Keqiang Yan, and Shuiwang Ji. "Graphdf: A discrete flow model for molecular graph generation." International Conference on Machine Learning. PMLR, 2021. [[paper]](https://proceedings.mlr.press/v139/luo21a.html) [[code]](https://github.com/lakshayguta/BTP/tree/378aac3ae9620aac43a995bcbfb71288593a04c9/DIG-main/dig/ggraph/GraphDF) 
- [ICML 2020] [RationaleRL] Jin, Wengong, Regina Barzilay, and Tommi Jaakkola. "Multi-objective molecule generation using interpretable substructures." International conference on machine learning. PMLR, 2020. [[paper]](https://proceedings.mlr.press/v119/jin20b.html) [[code]](https://github.com/wengong-jin/multiobj-rationale) 
- [ICLR 2020] [GraphAF] Shi, Chence, et al. "Graphaf: a flow-based autoregressive model for molecular graph generation." arXiv preprint arXiv:2001.09382 (2020). [[paper]](https://arxiv.org/abs/2001.09382) [[code]](https://github.com/DeepGraphLearning/GraphAF) 
- [ICML 2020] [HierVAE] Jin, Wengong, Regina Barzilay, and Tommi Jaakkola. "Hierarchical generation of molecular graphs using structural motifs." International conference on machine learning. PMLR, 2020. [[paper]](https://proceedings.mlr.press/v119/jin20a.html) [[code]](https://github.com/wengong-jin/hgraph2graph/)
- [arXiv 2019] [GraphNVP] Madhawa, Kaushalya, et al. "Graphnvp: An invertible flow model for generating molecular graphs." arXiv preprint arXiv:1905.11600 (2019). [[paper]](https://arxiv.org/abs/1905.11600) [[code]](https://github.com/pfnet-research/graph-nvp)
- [NeurIPS 2018] [CGVAE] Liu, Qi, et al. "Constrained graph variational autoencoders for molecule design." Advances in neural information processing systems 31 (2018). [[paper]](https://proceedings.neurips.cc/paper/2018/hash/b8a03c5c15fcfa8dae0b03351eb1742f-Abstract.html) [[code]](https://github.com/drigoni/ConditionalCGVAE) 
- [NeurIPS 2018] Ma, Tengfei, Jie Chen, and Cao Xiao. "Constrained generation of semantically valid graphs via regularizing variational autoencoders." Advances in Neural Information Processing Systems 31 (2018). [[paper]](https://proceedings.neurips.cc/paper/2018/hash/1458e7509aa5f47ecfb92536e7dd1dc7-Abstract.html) 😢 No official codes are available. 
- [ICML 2018] [JT-VAE] Jin, Wengong, Regina Barzilay, and Tommi Jaakkola. "Junction tree variational autoencoder for molecular graph generation." International conference on machine learning. PMLR, 2018. [[paper]](https://proceedings.mlr.press/v80/jin18a.html) [[code]](https://github.com/wengong-jin/icml18-jtnn)
- [ICML 2018] [MolGAN] De Cao, Nicola, and Thomas Kipf. "MolGAN: An implicit generative model for small molecular graphs." arXiv preprint arXiv:1805.11973 (2018). [[paper]](https://arxiv.org/abs/1805.11973) [[code]](https://github.com/nicola-decao/MolGAN)

**UL-based & SSL-based generator - SMILES string**

- [Chem. Sci. 2021] [STONED] Nigam, AkshatKumar, et al. "Beyond generative models: superfast traversal, optimization, novelty, exploration and discovery (STONED) algorithm for molecules using SELFIES." Chemical science 12.20 (2021): 7079-7090. [[paper]](https://pubs.rsc.org/en/content/articlehtml/2021/sc/d1sc00231g) [[code]](https://github.com/aspuru-guzik-group/stoned-selfies) 
- [arXiv 2018] [ORGAN] Guimaraes, Gabriel Lima, et al. "Objective-reinforced generative adversarial networks (organ) for sequence generation models." arXiv preprint arXiv:1705.10843 (2017). [[paper]](https://arxiv.org/abs/1705.10843) [[code]](https://github.com/gablg1/ORGAN)
- [J Chem Inf Model 2018] [BIMODAL] Grisoni, Francesca, et al. "Bidirectional molecule generation with recurrent neural networks." Journal of chemical information and modeling 60.3 (2020): 1175-1183. [[paper]](https://pubs.acs.org/doi/full/10.1021/acs.jcim.9b00943) [[code]](https://github.com/ETHmodlab/BIMODAL) 
- [ACS Cent. Sci. 2018] [VSeq2Seq] Gómez-Bombarelli, Rafael, et al. "Automatic chemical design using a data-driven continuous representation of molecules." ACS central science 4.2 (2018): 268-276. [[paper]](https://pubs.acs.org/doi/10.1021/acscentsci.7b00572) [[unofficial code]](https://github.com/aksub99/molecular-vae) 😢 No official codes are available.
- [ACS Cent. Sci. 2018] Segler, Marwin HS, et al. "Generating focused molecule libraries for drug discovery with recurrent neural networks." ACS central science 4.1 (2018): 120-131. [[paper]](https://pubs.acs.org/doi/full/10.1021/acscentsci.7b00512) [[unofficial code]](https://github.com/jaechanglim/molecule-generator) 😢 No official codes are available.
- [ICML/PMLR 2017] [GVAE] Kusner, Matt J., Brooks Paige, and José Miguel Hernández-Lobato. "Grammar variational autoencoder." International conference on machine learning. PMLR, 2017. [[paper]](https://arxiv.org/abs/1703.01925) [[code]](https://github.com/mkusner/grammarVAE) 



## Small molecular optimization <a id="small_molecular_optimization"></a>

While both molecular generation and optimization involve creating new molecules, generation is focused on creating entirely new molecules from scratch, while optimization is focused on improving the properties of existing molecules.

- [ICLR 2019] Jin, Wengong, et al. "Learning multimodal graph-to-graph translation for molecular optimization." arXiv preprint arXiv:1812.01070 (2018). [[paper]](https://arxiv.org/abs/1812.01070) [[code]](https://github.com/wengong-jin/iclr19-graph2graph) 
- [Sci. Rep. 2019] [MolDQN] Zhou, Zhenpeng, et al. "Optimization of molecules via deep reinforcement learning." Scientific reports 9.1 (2019): 1-10. [[paper]](https://arxiv.org/abs/1810.08678) [[code]](https://github.com/google-research/google-research/tree/master/mol_dqn) 

