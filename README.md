# HiGPT_athnaik

## 1. Environment Preparation (Python 3.10, CUDA 11.7)

First, set up a virtual environment for the project:

```bash
python -m venv higpt_env
source higpt_env/bin/activate

pip install torch==1.13.0+cu117 torchvision==0.14.0+cu117 torchaudio==0.13.0 --extra-index-url https://download.pytorch.org/whl/cu117
pip3 install "fschat[model_worker,webui]"
pip install torch_geometric
pip install pyg_lib -f https://data.pyg.org/whl/torch-1.13.0%2Bcu117/pyg_lib-0.4.0%2Bpt113cu117-cp310-cp310-linux_x86_64.whl
pip install torch_scatter -f https://data.pyg.org/whl/torch-1.13.0%2Bcu117/torch_scatter-2.1.1%2Bpt113cu117-cp310-cp310-linux_x86_64.whl
pip install torch_cluster -f https://data.pyg.org/whl/torch-1.13.0%2Bcu117/torch_cluster-1.6.1%2Bpt113cu117-cp310-cp310-linux_x86_64.whl
pip install torch_sparse -f https://data.pyg.org/whl/torch-1.13.0%2Bcu117/torch_sparse-0.6.17%2Bpt113cu117-cp310-cp310-linux_x86_64.whl
pip install torch_spline_conv -f https://data.pyg.org/whl/torch-1.13.0%2Bcu117/torch_spline_conv-1.2.2%2Bpt113cu117-cp310-cp310-linux_x86_64.whl

git clone <repository-url>
cd HiGPT
pip install -r requirements_updated.txt
```


## 2. Update Paths inside script files and model file

In higpt_stage_1.sh, extract_projector.sh, higpt_stage_2.sh, and higpt_info_imdb_cot.sh files update cache, tmp, and root path directories in first 4 lines.

Update train_hete_nopl.py file on line 817, add root path to HiGPT directory.


