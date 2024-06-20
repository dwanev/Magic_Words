

# Getting Running on Mac with Conda

conda create -n magic_words python=3.11
python3 -m pip install -e .
python3 -m pip install -r requirements.txt
(venv uses deactivate to deactivate an environment)

Status 20/6/2024 
- I can run sgcg on my macbook, but I can not double-check I understand the code correctly (i.e. push the attack and prompt through the model as see the decoded output.)
- backoff_hack_demo.py throws a type exception on .backward(), deep in the code, not on the first call of this function. I have not worked out why.
- 

I have To get working on a macbook:
```bash
python3 scripts/sgcg.py \
    --dataset datasets/100_squad_train_v2.0.jsonl \
    --model meta-llama/Meta-Llama-3-8B-Instruct \
    --k 20 \
    --max_parallel 3 \
    --grad_batch_size 5 \
    --num_iters 30
    
```

