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
- Jupyter
- spaces and punctuation -- what do they mean?
- variables and data types

my_name = 'Mike'
my_age = 38
my_license_plate = 'DWZ 147'

- operators
addition vs. concatenation
2 + 2
'Hello' + 'world'
'2' + '2'

= vs. ==
2 + 2 == 4
2 + 2 == 5
2 + 2 != 5

- conditionals

my_num = 2
if my_num == 6:
    print('Yes, it does.')

else:
    print('No, that would make no sense.')

- iterables
my_list_of_nums = [2, 3, 1, 7, 894]
my_list_of_dog_names = ['Reggie', 'Sadie', 'Charlotte']

- loops
for thingy in my_list_of_nums:
    print(thingy)

for thingy in my_list_of_dog_names:
    print(thingy)

total = 0
for thingy in my_list_of_nums:
   total += thingy
total

- Functions and methods

A function is a little factory: You put raw materials in, do some work, and something comes out.

def my_factory(first_ingredient, second_ingredient):
  final_product = first_ingredient + second_ingredient
  return final_product

my_factory(2, 2)
my_factory(7, 3)

- Pandas/what are modules
import pandas as pd

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
# First, test to see what might already be installed
brew install  # If it doesn't say "command not found" brew might already be installed
pip install  # If it doesn't say "command not found" pip might already be installed

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update

brew install pip  # Not sure if this will cover the pyenv pip or not -- we'll find out!
# Or, if brew install pip doesn't work...
brew install python # Don't do this if brew install pip worked.

brew install pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile
exec "$SHELL"
# (Open new Terminal tab)
pyenv install 3.7.0
brew install pyenv-virtualenv
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bash_profile
exec "$SHELL"
# (Open new Terminal tab)
pyenv virtualenv 3.7.0 jupyterpandas
mkdir ~/Documents/Reveal
cd ~/Documents/Reveal/
# (Sign up for github account if you dont' have one.)
git config --global user.name "Human readable name"
git config --global user.email "email@email.com"
git clone https://github.com/cirlabs/JupyterPandasTraining.git
cd JupyterPandasTraining
pip install -r requirements.txt
```
