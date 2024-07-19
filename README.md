# Mask-identification
由於疫情嚴峻

台灣中央流行疫情指揮中心表示民眾在出入無法保持社交距離、或會密切接觸不特定對象之人潮擁擠或密閉場所時，務必佩戴口罩  

辨識是否佩戴口罩成為公共場所須具備的功能

為達到AI影像辨識

在此使用YOLOv4 模型進行建模

## YOLO (You Only Look Once) 
YOLO為建立一個 real time 且 high performance 的 物件偵測 (Object Detection) 

物件偵測可應用在生活中的各種事物，例如:
1. 瑕疵偵測：可做為工業辨識產品好壞  

2. 車流偵測: 計算車輛數量，偵測車流  

3. 人臉偵測：辨識人臉  


YOLOv4 的網路架構圖:

![image](https://user-images.githubusercontent.com/64676970/151686241-63ed0e91-d595-488b-8086-4a8e5c6b4ec1.png)


## 成果

在這裡使用yolo物件偵測來辨識照片中的人物是否佩戴口罩

***原圖:***

![image](https://user-images.githubusercontent.com/64676970/151685759-0c9ef34a-67b7-4051-8ff2-0f5891b13fab.png)

***經過訓練之模型，預測出的結果:***

![image](https://user-images.githubusercontent.com/64676970/151685770-30430d88-9cca-4aaa-a677-1b6874cb4953.png)

***輸出數據:***

```
/content/test.jpg: Predicted in 100.542000 milli-seconds.
good: 94%
good: 83%
good: 98%
good: 98%
good: 98%

```
在人物清楚沒有重疊的狀態下，此模型可以有高信心能辨識出人物是否有配戴口罩

但在人物眾多且有非正面以及交錯的狀態下，還是會辨識錯誤
