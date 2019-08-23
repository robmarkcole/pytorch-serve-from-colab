## pytorch-serve-from-colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/robmarkcole/pytorch-serve-from-colab/blob/master/pytorch-serve-colab.ipynb)

* Serve up a pytorch model via flask and access on a publix URL [via ngrok](https://github.com/gstaff/flask-ngrok)
* Use as a research tool for batch processing or just as an on demand services, all GPU accelerated :) Be sure to read the [Colab FAQ](https://research.google.com/colaboratory/faq.html)

## Run on colab
Open the notebook on [colab](https://colab.research.google.com) by clicking on the `Open In Colab` button above and follow the instructions to mount your Google drive. Then you can make a request from anywhere on the internet (substituting the ngrok url below for your own) e.g:
```
curl -X POST -F file=@hummingbird.jpg http://6801b5e1.ngrok.io/predict
```

## Run app locally
Run the flask app, this requires sudo on my machine:
```
sudo python3 app.py 
```
Check that the app is accessible on the ngrok url. Then make a prediction:
```
curl -X POST -F file=@hummingbird.jpg http://localhost:5000/predict

{
  "class_id": "n01833805", 
  "class_name": "hummingbird"
}
```