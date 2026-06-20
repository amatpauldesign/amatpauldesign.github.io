[![Back home](https://img.shields.io/badge/%E2%AC%85%20Back%20home-blue)](index.html)

# snippets

## Managing GitHub accounts with GitHub CLI

Install gh

```bash
brew install gh
```

To be done for each account

```bash
gh auth login
```

Inside the local directory that uses the personal account

```bash
git config --local user.email "amatpaul@gmail.com"
```

Inside the local directory that uses the professional account

```bash
git config --local user.email "mail@pro.com"
```

Verify with

```bash
git config user.email
```

Tell Git to use gh for authentication

```bash
gh auth setup-git
```

To see active or inactive accounts

```bash
gh auth status
```

Switch from one account to another

```bash
gh auth switch --user your_username
```

Remove an account from the machine

```bash
gh auth logout
```

## Clone Python repository

Clone the repository

```bash
git clone (link)
```

Create a virtual environment

```bash
python3 -m venv .venv
```

Activate the virtual environment

```bash
source .venv/bin/activate
```

Verify which pip binary is being used

```bash
which pip
```

Upgrade pip

```bash
pip install --upgrade pip
```

Install dependencies from requirements file

```bash
pip install -r requirements.txt
```

## Managing branches

Create and switch to a new branch

```bash
git switch -c dev
```

Push the new branch and set upstream

```bash
git push -u origin dev
```

Force delete local branches

```bash
git branch -D dev dev2
```

## Commit, pull and push

Stage all changes

```bash
git add .
```

Commit changes with a message

```bash
git commit -m "Message"
```

Pull the latest changes from the remote repository

```bash
git pull
```

Push local commits to the remote repository

```bash
git push
```

## Deploy

Generate the 'requirements.txt' file

```bash
pip freeze > requirements.txt
```

Create a Docker build

```bash
docker build -t my_streamlit_app .
```

Test Docker build

```bash
docker build . -t test
```

Run the Docker container

```bash
docker run -p 8501:8501 my_streamlit_app
```

List available Docker images

```bash
docker images
```

Remove a Docker container after execution

```bash
docker run --rm -p 8501:8501 my_streamlit_app
```

Launch Pytest with PYTHONPATH

```bash
PYTHONPATH=src pytest -v
```

Launch Pytest and see the manually added print()

```bash
pytest -s
```
