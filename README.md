# stock-predictor
Homework assignment to demonstrate deployment of a model on AWS EC2 with Fast API

After creating an AWS EC2 instance do the following to set up the environment:
```
sudo yum update -y 
sudo yum install git -y  # install git

# install tmux to switch easily between programs in one terminal
sudo yum install tmux

# install miniconda and add its path to env
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
bash ~/miniconda.sh -b -p ~/miniconda
echo "PATH=$PATH:$HOME/miniconda/bin" >> ~/.bashrc
source ~/.bashrc
```

Use this to clone the repository:
```
git clone https://github.com/[YOUR HANDLER]/stock-predictor.git
cd stock-predictor
pip install -U pip
pip install -r requirements.txt
```

Use this to avoid SSH time out
`tmux new -s stock_session`

Now, run this command from the directory with main.py to run the app:
`uvicorn main:app --reload --workers 1 --host 0.0.0.0 --port 8000`

And, finally, in a new terminal window, use this command to get predictions: (replace the IP address with the one for the server instance)
```
curl \
--header "Content-Type: application/json" \
--request POST \
--data '{"ticker":"MSFT", "days":7}' \
http://34.223.219.65:8000/predict
```
