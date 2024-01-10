To run the run_summarization.py borrowed from huggingface implemenation, we introduce two custom parameters:
  1. tokenizer_type which could be {BART/PEGASUS}
  2. domain_token_path which is the path of updated model vocabulary.

We present an example of using the updated python  script as follows:
```
python run_summarization.py \
    --model_name_or_path facebook/bart-large \
    --do_train \
    --do_eval \
    --train_file Train_PubMed.csv \
    --validation_file valid_PubMed.csv \
    --output_dir ./BART_LARGE_PubMed_BioASQSubWords_15K_5/ \
    --per_device_train_batch_size=8 \
    --per_device_eval_batch_size=8 \
    --overwrite_output_dir \
    --evaluation_strategy steps \
    --eval_steps 2500 \
    --num_train_epochs 5 \
    --save_strategy steps \
    --save_steps 2500 \
    --load_best_model_at_end True \
    --save_total_limit 1 \
    --gradient_accumulation_steps 2 \
    --tokenizer_type BART \
    --domain_token_path ./BART-NewOOV-Configs/15000-5_BioASQ \
    --max_source_length 700 \
    --max_target_length 200 
```
