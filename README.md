# encoder-decoders
Use models like Llama as an encoder-decoder

## Models

- bert
- roberta
- gpt2
- [WIP] Llama
- [WIP] GPTBigCode

## Usage

```python

python run_seq2seq.py \
  --encoder_model_name_or_path "bert-base-cased" \
  --decoder_model_name_or_path "bert-base-cased" \
  --output_dir "bert-encoder-decoder" \
  --dataset_name samsum \
  --fp16 \
  --do_train \
  --do_eval \
  --overwrite_output_dir \
  --evaluation_strategy "epoch" \
  --logging_steps 10 \
  --predict_with_generate \
  --max_source_length 512 \
  --save_strategy "epoch" \
  --save_total_limit 1 \
  --per_device_train_batch_size 16
```