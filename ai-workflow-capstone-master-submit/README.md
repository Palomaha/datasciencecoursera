# AI Workflow 

This project uses time series to forecast revenue prediction for the next 30 days.

# Usage notes

All commands are from this directory.

## To test `api.py`

```bash
~$ python api.py
```

or to start the flask app in debug mode

```bash
~$ python api.py -d
```

Go to http://0.0.0.0:8080/ 

## To test the model directly and train the model

see the code at the bottom of `model.py`

```bash
~$ python model.py
```

## To build the docker container

```bash
~$ docker build -t ai-workflow .
```

Check that the image is there.

```bash
~$ docker image ls
```

delete the image

```bash
~$ docker image rm IMAGE_ID_OR_NAME
```

And every once and a while if you want clean up you can

```bash
~$ docker system prune
```

## Run the unittests

Before running the unit tests launch the `app.py`.

To run only the api tests

```bash
~$ python unittests/ApiTests.py
```

To run only the model tests

```bash
~$ python unittests/ModelTests.py
```

To run all of the tests

```bash
~$ python run-tests.py
```

## Run the container to test that it is working  

```bash
~$ docker run -p 4000:8080 ai-workflow
```

Go to http://0.0.0.0:4000/ 



