# Awesome Early Exiting Papers
A curated list of Early Exiting papers, benchmarks, and misc. Currently, the resources listed in this repo are mainly in the field of natural language processing. Adding papers of early exiting in other fields (*e.g.* computer vision) is also welcome. (This repo is constantly updated.)
> Early Exiting is an efficient technique that trains a deep model with multiple injected internal classifiers (exits) such that test samples can selectively exit instead of passing through the entire model.

## Contents

- [Contents](#contents)
- [Introduction](#introduction)
- [Benchmarks](#benchmarks)
- [Papers](#papers)
    - [Surveys](#surveys)
    - [Dynamic Methods](#dynamic-methods)
    - [Static Methods](#static-methods)
- [Contributing](#contributing)

## Introduction

Early exiting methods usually add internal classifiers to different layers of a model. By training these internal classifiers with the ground truth, the model has a chance to predict the correct label and exit earlier during inference. Current early exiting methods can be divided into two branches: 1. Dynamic methods and 2. Static methods.

**Dynamic Early Exiting** methods typically have two steps: (a) Training the internal classifiers on downstream tasks to make them capable of making predictions, (b) Designing an exiting strategy to decide whether to exit early or continue to the next layer.

**Static Early Exiting** methods assign each test sample to a specific layer by learning the difficulty of the samples or heuristically pre-defining the assignment of samples.

## Benchmarks

<img width="351" height="100" src="https://txsun1997.github.io/pictures/elue.png" alt="ELUE Benchmark"/>

**Towards Efficient NLP: A Standard Evaluation and A Strong Baseline**. NAACL 2022.

*Xiangyang Liu\*, Tianxiang Sun\*, Junliang He, Lingling Wu, Xinyu Zhang, Hao Jiang, Zhao Cao, Xuanjing Huang, Xipeng Qiu.* \[[pdf](https://txsun1997.github.io/papers/elue_paper.pdf)\][[website](http://eluebenchmark.fastnlp.top/)]

## Papers

### Surveys

1. **Dynamic Neural Networks: A Survey.** Preprint Feb 2021.

   *Yizeng Han, Gao Huang, Shiji Song, Le Yang, Honghui Wang, Yulin Wang.* [[pdf](https://arxiv.org/pdf/2102.04906.pdf)]
   
2. **A Survey on Dynamic Neural Networks for Natural Language Processing.** Preprint Feb 2022.

   *Canwen Xu, Julian McAuley.* [[pdf](https://arxiv.org/pdf/2202.07101.pdf)]

3. **Split Computing and Early Exiting for Deep Learning Applications: Survey and Research Challenges.** Preprint Mar 2021.

   *Yoshitomo Matsubara, Marco Levorato, Francesco Restuccia.* [[pdf](https://arxiv.org/pdf/2103.04505.pdf)]

4. **Adaptive Inference through Early-Exit Networks: Design, Challenges and Directions.** EMDL 2021.

   *Stefanos Laskaridis, Alexandros Kouris, Nicholas D. Lane.* [[pdf](https://arxiv.org/pdf/2106.05022.pdf)]
   
5. **A Survey on Green Deep Learning.** Preprint 2021.

   *Jingjing Xu, Wangchunshu Zhou, Zhiyi Fu, Hao Zhou, Lei Li.* [[pdf](https://arxiv.org/abs/2111.05193)] 

6. **Efficient Methods for Natural Language Processing: A Survey.** Preprint 2022.

   *Marcos Treviso, Tianchu Ji, Ji-Ung Lee, Betty van Aken, Qingqing Cao, Manuel R. Ciosici, Michael Hassid, Kenneth Heafield, Sara Hooker, Pedro H. Martins, André F. T. Martins, Peter Milder, Colin Raffel, Edwin Simpson, Noam Slonim, Niranjan Balasubramanian, Leon Derczynski, Roy Schwartz.* [[pdf](https://arxiv.org/abs/2209.00099)]
   
### Dynamic Methods

1. **DeeBERT: Dynamic Early Exiting for Accelerating BERT Inference.** ACL 2020.

   *Ji Xin, Raphael Tang, Jaejun Lee, Yaoliang Yu, and Jimmy Lin.* [[pdf](https://aclanthology.org/2020.acl-main.204.pdf)]

2. **The Right Tool for the Job: Matching Model and Instance Complexities.** ACL 2020.

   *Roy Schwartz, Gabriel Stanovsky, Swabha Swayamdipta, Jesse Dodge, and Noah A. Smith.* [[pdf](https://aclanthology.org/2020.acl-main.593.pdf)]

3. **FastBERT: a Self-distilling BERT with Adaptive Inference Time.** ACL 2020.

   *Weijie Liu, Peng Zhou, Zhiruo Wang, Zhe Zhao, Haotang Deng, and Qi Ju.* [[pdf](https://aclanthology.org/2020.acl-main.537.pdf)]

4. **Early Exiting BERT for Efficient Document Ranking.** ACL 2020.

   *Ji Xin, Rodrigo Nogueira, Yaoliang Yu, Jimmy Lin.* [[pdf](https://aclanthology.org/2020.sustainlp-1.11.pdf)]

5. **BERT Loses Patience: Fast and Robust Inference with Early Exit.** NeurIPS 2020.

   *Wangchunshu Zhou, Canwen X	u, Tao Ge, Julian McAuley, Ke Xu, Furu Wei.* [[pdf](https://proceedings.neurips.cc//paper/2020/file/d4dd111a4fd973394238aca5c05bebe3-Paper.pdf)]

6. **DynaBERT: Dynamic BERT with Adaptive Width and Depth.** NeurlPS 2020.

   *Lu Hou, Zhiqi Huang, Lifeng Shang, Xin Jiang, Xiao Chen, Qun Liu.* [[pdf](https://arxiv.org/pdf/2004.04037.pdf)]

7. **A Global Past-Future Early Exit Method for Accelerating Inference of Pre-trained Language Models.** NAACL 2021.

   *Kaiyuan Liao, Yi Zhang, Xuancheng Ren, Qi Su, Xu Sun, Bin He.* [[pdf](https://aclanthology.org/2021.naacl-main.162.pdf)]

8. **RomeBERT: Robust Training of Multi-Exit BERT.** Preprint Jan 2021.

   *Shijie Geng, Peng Gao, Zuohui Fu, Yongfeng Zhang.* [[pdf](https://arxiv.org/pdf/2101.09755.pdf)]

9. **BERxiT: Early Exiting for BERT with Better Fine-Tuning and Extension to Regression.** EACL 2021.

   *Ji Xin, Raphael Tang, Yaoliang Yu, Jimmy Lin.* [[pdf](https://aclanthology.org/2021.eacl-main.8.pdf)]

10. **Accelerating BERT Inference for Sequence Labeling via Early-Exit.** ACL 2021.

    *Xiaonan Li, Yunfan Shao, Tianxiang Sun, Hang Yan, Xipeng Qiu, Xuanjing Huang.* [[pdf](https://aclanthology.org/2021.acl-long.16.pdf)]

11. **LeeBERT: Learned Early Exit for BERT with Cross-Level Optimization.** ACL 2021.

    *Wei Zhu.* [[pdf](https://aclanthology.org/2021.acl-long.231.pdf)]

12. **TR-BERT: Dynamic Token Reduction for Accelerating BERT Inference.** ACL 2021.

    *Deming Ye, Yankai Lin, Yufei Huang, Maosong Sun.* [[pdf](https://aclanthology.org/2021.naacl-main.463.pdf)]

13. **EBERT: Efficient BERT Inference with Dynamic Structured Pruning.** ACL 2021.

    *Zejian Liu, Fanrong Li, Gang Li, Jian Cheng.* [[pdf](https://aclanthology.org/2021.findings-acl.425.pdf)]

14. **Class Means as an Early Exit Decision Mechanism.** Preprint Mar 2021.

    *Alperen Gormez, Erdem Koyuncu.* [[pdf](https://arxiv.org/pdf/2103.01148.pdf)]

15. **Early Exiting with Ensemble Internal Classifiers.** Preprint May 2021.

    *Tianxiang Sun, Yunhua Zhou, Xiangyang Liu, Xinyu Zhang, Hao Jiang, Zhao Cao, Xuanjing Huang, Xipeng Qiu.* [[pdf](https://arxiv.org/pdf/2105.13792.pdf)]

16. **ELBERT: Fast Albert with Confidence-Window Based Early Exit.** Preprint Jul 2021.

    *Keli Xie, Siyuan Lu, Meiqi Wang, Zhongfeng Wang.* [[pdf](https://arxiv.org/pdf/2107.00175.pdf)]

17. **CascadeBERT: Accelerating Inference of Pre-trained Language Models via Calibrated Complete Models Cascade.** EMNLP 2021.

    *Lei Li, Yankai Lin, Deli Chen, Shuhuai Ren, Peng Li, Jie Zhou, Xu Sun.* [[pdf](https://arxiv.org/pdf/2012.14682.pdf)]

18. **Consistent Accelerated Inference via Confident Adaptive Transformers.** EMNLP 2021.

    *Tal Schuster, Adam Fisch, Tommi Jaakkola, Regina Barzilay.* [[pdf](https://arxiv.org/pdf/2104.08803.pdf)]

19. **DACT-BERT: Differentiable Adaptive Computation Time for an Efficient BERT Inference.** Preprint Sep 2021.

    *Cristóbal Eyzaguirre, Felipe del Río, Vladimir Araujo, Álvaro Soto.* [[pdf](https://arxiv.org/pdf/2109.11745.pdf)]

20. **Towards Efficient NLP: A Standard Evaluation and A Strong Baseline**. NAACL 2022.

    *Xiangyang Liu\*, Tianxiang Sun\*, Junliang He, Lingling Wu, Xinyu Zhang, Hao Jiang, Zhao Cao, Xuanjing Huang, Xipeng Qiu.* \[[pdf](https://arxiv.org/pdf/2110.07038.pdf)\]

21. **GAML-BERT: Improving BERT Early Exiting by Gradient Aligned Mutual Learning.** EMNLP 2021

    *Wei Zhu, Xiaoling Wang, Yuan Ni, Guotong Xie.* [[pdf](https://aclanthology.org/2021.emnlp-main.242/)]
    
22. **PALBERT: Teaching ALBERT to Ponder.** NeurIPS 2022

    *Nikita Balagansky, Daniil Gavrilov.* [[pdf](https://arxiv.org/pdf/2204.03276.pdf)]  
    
23. **TangoBERT: Reducing Inference Cost by using Cascaded Architecture.** Preprint 2022

    *Jonathan Mamou, Oren Pereg, Moshe Wasserblat, Roy Schwartz.* [[pdf](https://arxiv.org/abs/2204.06271)]
   
24. **AdapLeR: Speeding up Inference by Adaptive Length Reduction.** ACL 2022

    *Ali Modarressi, Hosein Mohebbi, Mohammad Taher Pilehvar.* [[pdf](https://arxiv.org/abs/2203.08991)]
    
25. **BE3R: BERT based Early-Exit Using Expert Routing.** KDD 2022

    *Sourab Mangrulkar, S. AnkithM., Vivek Sembium.* [[pdf](https://dl.acm.org/doi/pdf/10.1145/3534678.3539132)]

26. **Confident Adaptive Language Modeling.** NeurIPS 2022

    *Tal Schuster, Adam Fisch, Jai Gupta, Mostafa Dehghani, Dara Bahri, Vinh Q. Tran, Yi Tay, Donald Metzler.* [[pdf](https://arxiv.org/abs/2207.07061)]
    
27. **COST-EFF: Collaborative Optimization of Spatial and Temporal Efficiency with Slenderized Multi-exit Language Models.** EMNLP 2022

    *Bowen Shen, Zheng Lin, Yuanxin Liu, Zhengxiao Liu, Lei Wang, Weiping Wang.* [[pdf](https://arxiv.org/abs/2210.15523)]
    
28. **E-LANG: Energy-Based Joint Inferencing of Super and Swift Language Models.** ACL 2022

    *Mohammad Akbari, Amin Banitalebi-Dehkordi, Yong Zhang.* [[pdf](https://arxiv.org/abs/2203.00748)]

29. **Length-Adaptive Transformer: Train Once with Length Drop, Use Anytime with Search.** ACL 2021

    *Gyuwan Kim, Kyunghyun Cho.* [[pdf](https://aclanthology.org/2021.acl-long.508/)]

30. **Model Cascading: Towards Jointly Improving Efficiency and Accuracy of NLP Systems.** EMNLP 2022

    *Neeraj Varshney, Chitta Baral.* [[pdf](https://arxiv.org/abs/2210.05528)]
    
31. **PCEE-BERT: Accelerating BERT Inference via Patient and Confident Early Exiting.** NAACL 2022

    *Zhen Zhang, Wei Zhu, Jinfan Zhang, Peng Wang, Rize Jin, Tae-Sun Chung.* [[pdf](https://aclanthology.org/2022.findings-naacl.25/)]
    
32. **Pyramid-BERT: Reducing Complexity via Successive Core-set based Token Selection.** ACL 2022

    *Xin Huang, Ashish Khetan, Rene Bidart, Zohar Karnin.* [[pdf](https://arxiv.org/abs/2203.14380)]
    
33. **SkipBERT: Efficient Inference with Shallow Layer Skipping.** ACL 2022

    *Jue Wang, Ke Chen, Gang Chen, Lidan Shou, Julian McAuley.* [[pdf](https://aclanthology.org/2022.acl-long.503/)]  

34. **Transkimmer: Transformer Learns to Layer-wise Skim.** ACL 2022

    *Yue Guan, Zhengyi Li, Jingwen Leng, Zhouhan Lin, Minyi Guo.* [[pdf](https://arxiv.org/abs/2205.07324)] 

35. **Unsupervised Early Exit in DNNs with Multiple Exits.** Preprint 2022

    *Hari Narayan N U, Manjesh K. Hanawal, Avinash Bhardwaj.* [[pdf](https://arxiv.org/abs/2209.09480)] 
    
36. **PoWER-BERT: Accelerating BERT Inference via Progressive Word-vector Elimination.** ICML 2020

    *Saurabh Goyal, Anamitra R. Choudhury, Saurabh M. Raje, Venkatesan T. Chakaravarthy, Yogish Sabharwal, Ashish Verma.* [[pdf](https://arxiv.org/abs/2001.08950)]

37. **Accelerating Inference for Pretrained Language Models by Unified Multi-Perspective Early Exiting.** COLING 2022

    *Jun Kong, Jin Wang, Liang-Chih Yu, Xuejie Zhang.* [[pdf](https://aclanthology.org/2022.coling-1.414.pdf)]
    
### Static Methods

1. **Depth-Adaptive Transformer.** ICLR 2020.

   *Maha Elbayad, Jiatao Gu, Edouard Grave, Michael Auli.* [[pdf](https://openreview.net/pdf?id=SJg7KhVKPH)]

2. **Faster Depth-Adaptive Transformers.** AAAI 2021.

   *Yijin Liu, Fandong Meng, Jie Zhou, Yufeng Chen, Jinan Xu.* [[pdf](https://arxiv.org/pdf/2004.13542.pdf)]
   
3. **A Simple Hash-Based Early Exiting Approach For Language Understanding and Generation**. Findings of ACL 2022.

    *Tianxiang Sun, Xiangyang Liu, Wei Zhu, Zhichao Geng, Lingling Wu, Yilong He, Yuan Ni, Guotong Xie, Xuanjing Huang, Xipeng Qiu* \[[pdf](https://arxiv.org/pdf/2203.01670.pdf)\]

## Contributing

:+1::tada: First off, thanks for taking the time to contribute! :tada::+1:

Steps to contribute:

- Make your awesome changes
- Submit pull request; if you add a new entry, please give a very brief explanation why you think it should be added.
