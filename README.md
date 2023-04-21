# helm-monitoring-example
Helm Chart Examples  
Monitoring Framework: Telegraf + InfluxDB + Chronograf
  
Install InfluxDB  
```  
helm install influxdb ./influxdb  
``` 
  
Install Telegraf    
```  
helm install telegraf ./telegraf  
``` 
  
Install Chronograf    
```  
helm install chronograf ./chronograf  
``` 
  
Check start-up    
```  
kubectl get pod 
kubectl get svc  
``` 
  
By default, the chronograph starts in ClusterIP mode  
To get access from outside it is necessary to redefine the type with the command  
```  
helm upgrade chronograf ./chronograf --set service.type=LoadBalancer
```  
  
If you are working in a minicube, you need to set the External IP  
```  
minicube service chronograf
```  