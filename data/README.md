# Codebase for IJCAI 

[BertSumAbs_Modified_Scripts](./BertSumAbs_Modified_Scripts/) contains the modified src folder w.r.t original [PreSumm](https://github.com/nlpyang/PreSumm) codebase.

[Transformers_Modified_Script](./Transformers_Modified_Script/) contains the modified version of [run_summarization.py](https://github.com/huggingface/transformers/blob/main/examples/pytorch/summarization/run_summarization.py) of the official huggingface codebase.

[GenerateSubwords](./GenerateSubwords/) contains the code for identifying words being split into four and more subwords, along with words thresholded on UMLS matching threshold for splits two and three.

[Vocabulary_Adaptation](./Vocabulary_Adaptation/) contains the code for generating the final ```DRIFT``` vocabulary that we add to the models.
