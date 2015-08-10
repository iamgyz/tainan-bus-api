# tainan-bus-api
An useful PHP script to provide user friendly JSON result for Tainan Bus realtime data  
With this api, you can get the realtime position of all the bus in Tainan !

### Install&Run  
```shell
git clone https://github.com/iamgyz/tainan-bus-api.git    
cd tainan-bus-api   
php -S 0.0.0.0:5566    
```
### Route parameter  

市區公車 route=city    
綠幹支線 route=green   
藍幹支線 route=blue   
棕幹支線 route=brown  
橘幹支線 route=orange  
黃幹支線 route=yellow  
紅幹支線 route=red  
觀光公車 route=travel  
高鐵公車 route=hsr  

### Usage  
`curl localhost:5566/bus.php?route=hsr`  

return:  

``` json
[
  {
    "route": "H62",
    "plate": "591-FS",
    "latitude": "22.975052",
    "longitude": "120.222400",
    "direction": "0"
  },
  {
    "route": "H62",
    "plate": "689-FS",
    "latitude": "22.971568",
    "longitude": "120.252270",
    "direction": "1"
  },
  {
    "route": "H62",
    "plate": "643-FM",
    "latitude": "23.015502",
    "longitude": "120.229548",
    "direction": "1"
  },
  {
    "route": "H62",
    "plate": "600-FS",
    "latitude": "22.976015",
    "longitude": "120.237042",
    "direction": "0"
  },
  {
    "route": "H62",
    "plate": "596-FS",
    "latitude": "23.004193",
    "longitude": "120.235508",
    "direction": "0"
  },
  {
    "route": "H31",
    "plate": "690-FS",
    "latitude": "22.989910",
    "longitude": "120.184362",
    "direction": "1"
  },
  {
    "route": "H31",
    "plate": "597-FS",
    "latitude": "22.965450",
    "longitude": "120.216350",
    "direction": "1"
  },
  {
    "route": "H31",
    "plate": "623-FS",
    "latitude": "22.927858",
    "longitude": "120.277158",
    "direction": "0"
  }
]
```
"route":路線編號  
"plate":車牌號碼  
"latitude":緯度  
"longitude":經度  
"direction": 0=>去程 1=>返程  

