# aws-hudi-delta-iceberg-interoperability
aws-hudi-delta-iceberg-interoperability
![Screenshot 2024-03-02 at 7 59 20 AM](https://github.com/soumilshah1995/aws-hudi-delta-iceberg-interoperability/assets/39345855/bc166c03-3757-4852-b71a-90fa7ab7c4ec)


# Steps 

### Step 1: Spin up the Stack 


### Configure GLue profile 
```
aws configure --profile glue4
```


### Edit the docker compose file 
```
    volumes:
#      -  C:\Users\soumilshah\.aws:/home/glue_user/.aws
      -  /Users/soumilshah/.aws:/home/glue_user/.aws
      - ./glue_jupyter_workspace:/home/glue_user/workspace/jupyter_workspace/
      - ./extra_python_path:/home/glue_user/workspace/extra_python_path/
```

### Run container 
```
docker-compose up --build -d
```

### Step 2: Create Hudi Table with the iPYNB Provided 


### Step 3: *  Download the Jar File and move the jar file into glue_jupyter_workspace folder
*  https://github.com/apache/incubator-xtable/packages/1986830
![image](https://github.com/soumilshah1995/aws-hudi-delta-iceberg-interoperability/assets/39345855/7cbad682-1817-4e8f-a44d-f05adc71897a)


```
java -jar  ./utilities-0.1.0-beta1-bundled.jar --dataset ./my_config.yaml

```

