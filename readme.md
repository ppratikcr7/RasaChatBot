### Rasa ChatBot:

#### Steps to setup rasa cli bot in your mac or linux system:

Create conda env:
conda create -n rasa-app python=3.6
conda env list
conda activate rasa-app

Upgrade pip:
pip3 install -U pip

Install Rasa open source:
pip3 install rasa

The first step is to create a new Rasa project. To do this, run:
rasa init
Press enter to create project in current directory

The rasa init command creates all the files that a Rasa project needs and trains a simple bot on some sample data.

This creates the following files:
__init__.py →an empty file that helps python find your actions
actions.py →code for your custom actions
config.yml ‘*’ →configuration of your NLU and Core models
credentials.yml →details for connecting to other services
data/nlu.md ‘*’ →your NLU training data
data/stories.md ‘*’ →your stories
domain.yml ‘*’ →your assistant’s domain
endpoints.yml →details for connecting to channels like fb messenger
models/<timestamp>.tar.gz →your initial model
The most important files are marked with a ‘*’. You will learn about all of these in this tutorial.

Next asked:
Do you want to train an initial model? 💪🏽 (Y/n)       Press Y

Next asked:
Do you want to speak to the trained assistant on the command line? 🤖 (Y/n) Press Y

Bot loaded. Type a message and press enter (use '/stop' to exit): 
Your input -> Hi

Separately train:
rasa train
echo "Finished training."

Run test cases:
rasa test
echo "Finished running tests."

The next step is to try it out! If you’re following this tutorial on your local machine, start talking to your assistant by running:
rasa shell

As we are heading towards building production-grade Rasa Chatbot setup, the first thing we can simply use the following command to start Rasa.
rasa run


#### To run UI:

Open two terminals and execute following cmds:

conda activate rasa-app
rasa run -m models --enable-api --cors "*" --debug
conda activate rasa-app
rasa run actions

Open index.html file


