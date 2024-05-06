
### Commands to execute
```shell
javac LambdaFunction.java

jar -cvf LambdaFunction.jar *.class
```

### Create the Lambda Function Using AWS CLI
```shell
aws lambda create-function --function-name LayersTestJava21AMD \
--zip-file fileb://target/demo-1.1.jar \
--handler example.LambdaFunction::handleRequest \
--runtime java21 \
--architectures x86_64 \
--role arn:aws:iam::466768951184:role/nr_extension_test_lambda_execution_role
```
### Update function
```shell
aws lambda update-function-code --function-name LayersTestJava21AMD \
--zip-file fileb://target/demo-1.1.jar
```