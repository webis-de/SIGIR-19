## SIGIR-19-ArgSearch Dataset
The study consists of 4 separate datasets. Their structure is given below. Each key represents a column name, with details about the contained data in the explanation field. Primary keys are marked in **bold**. If a combined key is used, all entries that the combined key is composed of are marked. Foreign keys that can be used to reference other tables are marked in *italics*.

###### Argument Dataset
| Key                 | Explanation                                                                                       |
|---------------------|---------------------------------------------------------------------------------------------------|
| ***Topic ID***      | Unique identifier for the topic context the item was judged in                                    |
| **Argument ID**     | Unique identifier for the item in regards to the discussion it is part of                         |
| **Discussion ID**   | Unique identifier of the discussion the item is part of                                           |
| Is Argument?        | Boolean value, indicating wether the item is an argument, or not                                  |
| Stance              | Denotes the stance of the item, can be Pro, Con or Not specified                                  |
| Relevance           | Relevance score as judged by the annotator, on a scale of 1 (not relevant) to 4 (very relevant)   |
| Logical Quality     | Logical quality score as judged by the annotator, on a scale of 1 (very bad) to 4 (very good)     |
| Rhetorical Quality  | Rhetorical quality score as judged by the annotator, on a scale of 1 (very bad) to 4 (very good)  |
| Dialectical Quality | Dialectical quality score as judged by the annotator, on a scale of 1 (very bad) to 4 (very good) |
| Premise             | Text of the items' premise                                                                        |
| Conclusion          | Text of the items' conclusion                                                                     |
| Comment             | Optional Comment made by the annotator                                                            |

###### Ranking Dataset
| Key               | Explanation                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| ***Topic ID***    | Unique identifier for the topic context                                       |
| **Engine**        | Name of the engine the ranking this entry stems from was obtained with        |
| **Rank**          | The rank of the argument in the respective engines ranking                    |
| *Argument ID*     | Unique identifier for the argument in regards to the discussion it is part of |
| *Discussion ID*   | Unique identifier of the discussion the argument is part of                   |

###### Annotator Dataset 
| Key               | Explanation                              |
|-------------------|------------------------------------------|
| ***Topic ID***    | ID of the topic judged by this annotator |
| Age               | Age of the annotator                     |
| Gender            | Gender of the annotator                  |
| Comment           | Annotators’ comments about the study     |

###### Topic Dataset
| Key                       | Explanation                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ***Topic ID***            | Unique identifier for the topic                                                                                                                                                                                                               |
| Biased                    | Boolean value indicating whether the topic is biased or not, i.e. if the annotator was tasked to adopt a predetermined stance (topic thesis)                                                                                                  |
| Annotator Stance          | Stance of the annotator, can be *I agree*, *I disagree* or *Neutral*; if the topic is biased, the stance is determined in regards to the topic description; if the topic is unbiased, the stance is determined in regards to the topic thesis |
| Thesis                    | Predetermined stance for unbiased topics, empty otherwise                                                                                                                                                                                     |
| Description               | Text description of the topic                                                                                                                                                                                                                 |
| Query                     | Query used for this topic as input for the retrieval models                                                                                                                                                                                   |


