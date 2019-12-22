# Micro Services - Spring Cloud Config 


## Running the Config Service

```
cd config-service
mvn clean package
java -jar target/config-service-0.0.1-SNAPSHOT.jar (starts on port 8888)
```
Url
```
http://localhost:8888/bank-account-service/uat
http://localhost:8888/bank-account-service/dev
http://localhost:8888/bank-account-service/default
```

## Running the Bank Account Service
```
cd bank-account-service
mvn clean package
java -jar target/bank-account-service-0.0.1-SNAPSHOT.jar (starts on port 8080)

```
Url- localhost:8080/bank-account (POST Method )
```
Content-Type: application/json
Body: {"accountId":"B12345","accountName":"Rajnish","accountType":"CURRENT_ACCOUNT","accountBlance":1250.38}
```

Url
```
localhost:8080/bank-account/{accountId} (GET Method)
```

## Testing the Bank Account Service: Curl
You can test the bank account service configuration by creating a new account. This will use the configuration pulled from the config service. 
```
curl -i -H "Content-Type: application/json" -X POST -d '{"accountId":"B12345","accountName":"Joe Bloggs","accountType":"CURRENT_ACCOUNT","accountBlance":1250.38}' localhost:8080/bank-account

Curl localhost:8080/bank-account/{accountId}
```

