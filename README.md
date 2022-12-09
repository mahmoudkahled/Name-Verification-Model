# Name-Verification-Model
## Description
The task is divided into multiple stages (Data generation - Core model - Interface - containerization).
The core stage of the task pipeline is name verification model with confidence threshold of how much the
name is real.

For example:
1. The name "باسم وحيد السيد" is a real name with high confidence.
2. The name "باسمم وحةد السد" “is a real name with low confidence.

## Instructions

### How to build the docker image
To build the Docker Image we should execute the following docker-compose command
```
docker-compose -f docker-compose.yaml up
```
After completion of building the last part in the output in the terminal should be as following 
```
task                              | INFO:     Started server process [1]
task                              | INFO:     Waiting for application startup.
task                              | INFO:     Application startup complete.
task                              | INFO:     Uvicorn running on http://0.0.0.0:80 (Press CTRL+C to quit)
```
**So, in this case the app has been built successfully!**

### How to test the solution

There is two ways to test the solution 
1. At this point the app was built and the connection to the  server is active now, so we can head now to the server by opening the browser and type this **URL** in the search bar
```
http://localhost:80/docs
```
2. Another way you can head to the server, is to open the **Docker Desktop Application** if it was installed on your local machine, you can open it then on the left press on **Containers**, then you will see our container expand it, then head to the **PORT(S)** column, and you will see this port **80:80**, then press on it and it will get you directly to the server to test

### How to verify results claimed
After you open the server, open the **GET Tab** that its name is **/Inference**, then press on **try it out** to let you enter some inputs, after you enter your full name to test, press on **Execute**, after that in the **Response body** you will see the results of the **Prediction of the model** and the **Execution Time**, as if the name was correct the result will be **The Full Name is: Correct**, and if the name was incorrect the result will be **The Full Name is: Correct**

so enter your test name and see the results of the model and see if the predection was right :)


