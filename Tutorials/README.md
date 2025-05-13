# [Tutorials](https://huggingface.co/docs/huggingface_hub/v0.13.2/en/guides/overview)


### [Installation](https://huggingface.co/docs/huggingface_hub/v0.13.2/en/installation)

```bash
# cmd

conda create --name huggingface python=3.10 -y
conda activate huggingface
```

```bash
# cmd

pip install --upgrade huggingface_hub ipykernel
```

```bash
# cmd

# Install dependencies for CLI-specific features.
pip install 'huggingface_hub[cli]'

# Install dependencies for tensorflow-specific features
pip install 'huggingface_hub[tensorflow]'

# Install dependencies for both torch-specific and CLI-specific features.
pip install 'huggingface_hub[torch]'
```


### [Getting your API Token](https://huggingface.co/docs/huggingface_hub/main/en/quick-start)

```bash

1.) create a huggingface account
2.) go to profile -> settings -> access tokens
3.) provide your credentials to create a api token
4.) create new token
5.) specify token name and privileges 
6.) safely store your api token (somewhere)
```

```bash
# Windows

# Either store the api token under your account environmental variables
1.) go to "Edit environmental variables for your account"
2.) select "New"
3.) set "Variable name" to HF_TOKEN
4.) set "Value value" to your api token
5.) press "Ok" and restart any open terminals
```

```bash
# cmd

# Using the provided interface
huggingface-cli login

# Or using an environment variable (same as above, but via commandline)
huggingface-cli login --token api_token_here --add-to-git-credential
```

To confirm that it is stored properly, run the following within a commandline terminal:

```bash
# cmd

huggingface-cli whoami
```

### [Download](https://huggingface.co/docs/huggingface_hub/v0.13.2/en/guides/download)

#### Model

#### Dataset

```python
# python

from huggingface_hub import hf_hub_download, snapshot_download

# Download a file from the dataset (README.md)
hf_hub_download(repo_id="ylecun/mnist", repo_type="dataset", filename="README.md")

# Download the whole repository (at a specific revision, point in time)
snapshot_download(repo_id="ylecun/mnist", repo_type="dataset", revision="refs/pr/1")

# Download the whole dataset to a specific location 
snapshot_download(repo_id="ylecun/mnist", repo_type="dataset", revision="refs/pr/1", local_dir="../Data")
```

#### Repository

```python
# python

```
