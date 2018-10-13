# An intro to data analysis with programming

### Class steps
- What is programming?
  - Telling your computer what to do, generally using written instructions called code
- How is your computer put together?
  - GUI vs no GUI
  - Wizard of OZ -- now you are the wizard
- Your friend, the command line
- Your shape-shifting, loyal best friend, the prompt (alebrije?)
- cd, ls stuff from TechRaking
- What is a program?
  - A set of written instructions
  - A recipe written like a poem

  The worst poems ever written

  there's nothing like the feeling unique
  when you find the record you seek

  read me a line of the spreadsheet, please
  tell me about infectious disease!

- Ways to run code
  - Shell
  - File

```python
print('See Jane run.')
print('Run, Jane, run.')
print("Run the program many times until it doesn't crash.")
```
- Errors are good now.
  - Read from the bottom up
  - Look for things that are your fault
- What are modules?
- Jupyter
- spaces and punctuation -- what do they mean?
- variables and data types
- iterables
- loops
- Functions and methods
- Pandas
- Read a CSV
- Join/Merge
- Group by
- Sort
- Basic chart

### Bootstrapping steps
We have installed several software packages in order to conduct the training and so you can work with these tools on your own.

- pip
- pyenv
- pyenv-virtualenv
- pandas
- vega
- altair

#### Step-by-step instructions to reproduce the environment (Mac-only)

- Mac dev tools/Xcode thingy
- build-essential
- homebrew
- pip

- Dependencies?
- Check out repository
- install requirements.txt


```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
brew install pip  # Not sure if this will cover the pyenv pip or not -- we'll find out!
brew install pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile
exec "$SHELL"
pyenv install 3.7.0
brew install pyenv-virtualenv
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bash_profile
exec "$SHELL"
pyenv virtualenv 3.7.0 jupyterpandas
mkdir ~/Documents/Reveal
cd ~/Documents/Reveal/
git clone git@github.com:cirlabs/JupyterPandasTraining.git
cd JupyterPandasTraining
pip install -r requirements.txt
```
