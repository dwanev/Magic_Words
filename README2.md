

# Getting Running on Mac with Conda

conda create -n magic_words python=3.11
python3 -m pip install -e .
python3 -m pip install -r requirements.txt
(venv uses deactivate to deactivate an environment)


To get working on a mac:
```bash
python3 scripts/sgcg.py \
    --dataset datasets/100_squad_train_v2.0.jsonl \
    --model meta-llama/Meta-Llama-3-8B-Instruct \
    --k 20 \
    --max_parallel 3 \
    --grad_batch_size 5 \
    --num_iters 30
    
```

