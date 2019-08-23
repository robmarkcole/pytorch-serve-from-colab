* Serve up pytorch model via flask -> https://github.com/robmarkcole/pytorch-flask-api
* Access over internet via ngrok -> https://github.com/gstaff/flask-ngrok
* Use for batch processing or just as an on demand services, all GPU accelerated

## Run on colab
Open the notebook on colab, upload the labels file and run all

## Run app locally
Run the flask app:
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