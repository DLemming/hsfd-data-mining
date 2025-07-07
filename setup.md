# How to reproduce results

- use Python 3.7 (3.7.9 in my case)
- create a .venv
- Install:
    - pandas>=1.1.5
    - scikit-learn>=1.0.2
    - anchor-exp
    - xgboost
- Clone the [LORE repository](https://github.com/rinziv/LORE_ext)
- In python files using lore (e.g. tabular/lore/lore_application_general.py), append sys-path with lore src:
    ```sh
    import sys
    sys.path.append("/home/david/dev/code/LORE_ext/src")
    ```
- Install dependencies for lore:
    - bitarray>=3.4.2
    - catboost==0.26
- Remove import of ```mixed_distance_idx``` in ```lore_application_general.py```


uv python version 3.8
uv init
uv venv
uv add anchor-exp
uv add "xgboost<1.3"
uv add "pandas<2.0"
uv add numpy scikit-learn ipykernel



# Todo for final presentation

## Objective: Compare ANCHOR to LORE on the german credit dataset
1. Get both Anchor and Lore running (not hard)
2. 


# Reproduction nightmare:
- Adult dataset: 
    - Unclear where they have it from. They say UCI
    ... but original DS has around 47,5k rows
    ... their dataset has only 30k rows
    - Their dataset doesn't contain their own examples from the paper (x1/x2)
    - x1's target doesn't align with what they claim in the paper
    - These idiots didn't use a fixed seed for splitting train/test
        - Wouldn't be a problem, if they actually used the datasets provided in the repo, but they didn't
    - Their provided datasets and models expected columns do not match
        => Thus using custom trained models on their datasets