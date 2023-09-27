# LLM / Graph AI / Knowledge Graph Experiments for Natural Language is all a Graph Needs

This project contains experiments on the ideas introduced in [Natural Language is all a Graph Needs](https://arxiv.org/abs/2308.07134) by [Ruosong Ye](https://www.linkedin.com/in/ruosong-ye-a0507724b/), [Caiqi Zhang](https://www.linkedin.com/in/caiqi-alex-zhang-%E5%BC%A0%E8%94%A1%E5%90%AF-99074519b/), [Runhui Wang](https://www.linkedin.com/in/runhui-wang/), [Shuyuan Xu](https://www.linkedin.com/in/shuyuan-xu-870206158/) and [Yongfeng Zhang](https://www.linkedin.com/in/zhangyongfeng/). LLMs have achieved such ease of use that the authors of the paper were able to release _just the prompts_ used for training rather than the entire codebase. This project is an attempt to reproduce the results of the paper and to explore the ideas introduced in the paper further via applied research into applying it to real-world problems.

## Blog Post Series

This work comes from a 3-part series of LinkedIn Articles:

* [LLMs-represent->Knowledge Graphs](https://www.linkedin.com/pulse/instructglm-knowledge-graphsrepresentedbyllms-russell-jurney/?trackingId=slyb9SVqTeemAVP8d4Zz5Q%3D%3D) - describes InstructGLM and announcs my intention to reproduce and extend it to entity resolution problems.
* 

## Essential Figures

To understand the paper, take a quick look at the following figures:

## Instruction Prompts (Appendix A.1)

Copied from the paper, the specification for the instruction prompts included in prompts.json are as follows:

    In this appendix, we present all our designed instruction prompts. It is worth noting that we follow
    the following conventions when numbering the prompts:

    • The length of each prompt number is 4.
    • The first digit represents the task index, where 1 represents the node classification task and 2
    represents the link prediction task.
    • The second digit represents whether node features or edge features (such as text information) other
    than numerical feature embedding are used in the prompt. 1 means not used and 2 means used.
    • The third digit represents the maximum hop order corresponding to the structural information
    considered in this prompt. 1 represents only the 1-hop neighbors are included, while 2 and 3
    represent the structural information including 2-hop and 3-hop neighbors, respectively.
    • The fourth digit represents whether the intermediate node information (i.e. the path) in the highorder connection is considered in this prompt. If the digit is even, it means that the intermediate
    node is considered, while an odd digit indicates otherwise.
    • Specially, in node classification task, we designed a graph-structure-free prompt and numbered it
    as 1-0-0-0.
