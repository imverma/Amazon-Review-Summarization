# Analytics on Amazon Reviews


#### Web demo

<img src="https://github.com/avivace/reviews-sentiment/blob/develop/figures/ext/webapp1.png">

<img src="https://github.com/avivace/reviews-sentiment/blob/develop/figures/ext/webapp2.png">

<img src="https://github.com/avivace/reviews-sentiment/blob/develop/figures/ext/webapp3.png">

<img src="https://github.com/avivace/reviews-sentiment/blob/develop/figures/ext/webapp4.png">

<img src="https://github.com/avivace/reviews-sentiment/blob/develop/figures/ext/webapp_plot2.png">

<img src="https://github.com/avivace/reviews-sentiment/blob/develop/figures/ext/webapp_plot1.png">

<img src="https://github.com/avivace/reviews-sentiment/blob/develop/figures/ext/webapp_plot3.png">



## Run

Set up the a Python virtual environment and install required packages

```bash
cd scripts
python3 -m venv .
source bin/activate
pip3 install -r requirements.txt
python3 -m spacy download en
```

Optionally, install a ipynb kernel to use the venv packages
```bash
pip3 install --user ipykernel
python -m ipykernel install --user --name=myenv
# Check the installed kernels
jupyter kernelspec list
# Run Jupyter
jupyter lab
```


Now, to run the full pipeline:
```bash
python3 main.py
```

A Flask application exposes a simple API (on port 5000) allowing the trained models to be used on demand via simple HTTP requests (in main.py). The VueJS application needs a recent version of NodeJS and npm.

```bash
cd webapp
npm install
# serve the web application with hot reload at localhost:8080/reviews-sentiment
npm run serve
# builds the web application for production
npm run build
# deploys the build on the master branch, making github serve it on https://avivace.github.io/reviews-sentiment
npm run deploy
```

