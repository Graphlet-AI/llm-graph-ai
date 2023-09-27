# Prompts from [Natural Language is all a Graph Needs](https://arxiv.org/abs/2308.07134) by [Ruosong Ye](https://www.linkedin.com/in/ruosong-ye-a0507724b/), [Caiqi Zhang](https://www.linkedin.com/in/caiqi-alex-zhang-%E5%BC%A0%E8%94%A1%E5%90%AF-99074519b/), [Runhui Wang](https://www.linkedin.com/in/runhui-wang/), [Shuyuan Xu](https://www.linkedin.com/in/shuyuan-xu-870206158/) and [Yongfeng Zhang](https://www.linkedin.com/in/zhangyongfeng/).

## A.1.1 Node Classification

### Task-Specific Prefix

```
Classify the paper according to its topic into one of the following categories: {{All Categories}} .\n Node represents academic paper with a specific topic, link represents a citation between the two papers. Pay attention to the multi-hop link relationship between the nodes.
```

### Prompt ID: 1-1-1-1

#### Input Template

```
{{central node}} is connected with {{1-hop neighbor list}} within one hop. Which category should {{central node}} be classified as?
```

#### Target Template

```
{{category}}
```

### Prompt ID: 1-1-2-1

#### Input Template

```
{{central node}} is connected with {{2-hops neighbor list}} within two hops. Which category should {{central node}} be classified as?
```

#### Target Template

```
{{category}}
```

### Prompt ID: 1-1-2-2

#### Input Template

```
{{central node}} is connected with {{2-hops neighbor list}} within two hops through {{corresponding 1-hop intermediate node list}}, respectively. Which category should {{central node}} be classified as?
```

#### Target Template

```
{{category}}
```

### Prompt ID: 1-1-3-1

#### Input Template

```
{{central node}} is connected with {{3-hops neighbor list}} within three hops. Which category should {{central node}} be classified as?
```

#### Target Template

```
{{category}}
```

### Prompt ID: 1-1-3-2

#### Input Template

```
{{central node}} is connected with {{3-hops neighbor list}} within three hops through {{corresponding 2-hops intermediate path list}}, respectively. Which category should {{central node}} be classified as?
```

#### Target Template:

```
{{category}}
```

### Prompt ID: 1-2-1-1

#### Input Template

```
({{central node}}, {{text feature}} ) is connected with {{1-hop neighbor list attached text feature}} within one hop. Which category should ({{central node}}, {{text feature}}) be classified as?
```

#### Target Template

```
{{category}}
```

### Prompt ID: 1-2-2-1

#### Imput Template

```
({{central node}},{{text feature}}) is connected with {{2-hops neighbor list attached text feature}} within two hops. Which category should ({{central node}},{{text feature}}) be classified as?
```

#### Target Template

```
{{category}}
```

### Prompt ID: 1-2-2-2

#### Input Template

```
({{central node}},{{text feature}}) is connected with {{2-hops neighbor list attached text feature}} within two hops through {{corresponding 1-hop intermediate node list attached text feature}}, respectively. Which category should ({{central node}},{{text feature}}) be classified as?
```

#### Target Template

```
{{category}}
```

### Prompt ID: 1-2-3-1

#### Input Template

```
({{central node}},{{text feature}}) is connected with {{3-hops neighbor list attached text feature}} within three hops. Which category should ({{central node}},{{text feature}}) be classified as?
```

#### Target Template

```
{{category}}
```


### Prompt ID: 1-2-3-2

#### Input Template

```
({{central node}},{{text feature}}) is connected with {{3-hops neighbor list attached text feature}} within three hops through {{corresponding 2-hops intermediate path list attached text feature}}, respectively. Which category should ({{central node}},{{text feature}}) be classified as?
```

#### Target Template

```
{{category}}
```

### Prompt ID: 1-0-0-0

#### Input Template

```
{{central node}} is featured with {{central node}} be classified as?
```

#### Target Template

```
{{category}}
```

## A.1.2 Link Prediction

### Task-Specific Prefix

```
Perform Link Prediction for the central node:\n Node represents academic paper with a specific topic, link represents a citation between the two papers. Pay attention to the multi-hop link relationship between the nodes.
```

### Prompt ID: 2-1-1-1

#### Input Template

```
{{central node}} is connected with {{1-hop neighbor list}} within one hop. Will
{{candidate node}} be connected with {{central node}} within one hop? 
```

#### Target Template

```
{{yes_no}}
```

### Prompt ID: 2-1-1-2

#### Input Template

```
{{central node}} is connected with {{1-hop neighbor list}} within one hop. Which other node will be connected to {{central node}} within one hop?
```

#### Target Template

```
{{node_id}}
```


### Prompt ID: 2-1-2-1

#### Input Template

```
{{central node}} is connected with {{2-hops neighbor list}} within two hops. Will {{ candidate node}} be connected to {{ central node}} within two hops?
```

#### Target Template

```
{{yes_no}}
```

### Prompt ID: 2-1-2-2

#### Input Template

```
{{central node}} is connected with {{ 2-hops neighbor list}} within two hops through {{corresponding 1-hop intermediate node list}}, respectively. Will {{candidate node}} be connected to {{central node}} within two hops through {{specified 1-hop intermediate node}}?
```

#### Target Template

```
{{yes_no}}
```

### Prompt ID: 2-1-2-3

#### Input Template

```
{{central node}} is connected with {{2-hops neighbor list}} within two hops. Which other node will be connected to {{central node}} within two hops?
```

#### Target Template

```
{{node_id}}
```

