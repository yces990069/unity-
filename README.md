# unity 學習日誌
2022/3月 正式接觸unity 跟著教學做了些有的沒的的小遊戲  
2022/9/5 頹廢整個暑假後開始繼續學  
2022/9/12 學習何謂四元數,嘗試只看unity api做出角色控制器  

2022/9/13 角色控制器完成?  
# 快速理解四元數Quaternion
其概念類似於stereographic projection,四元數是將四維度的圖形投射到三度空間上用以描述一物體在三度空間之選轉  
假設空間上有一點(x,y,z)沿著向量(vx,vy,vz)旋轉 $\theta$ 度
Rq(p)=qpq
四元數簡易概念教學 https://www.youtube.com/watch?v=d4EgbgTm0Bg

# 筆記
以下都是我從unityapi抓下來然後解析並白話的翻譯成中文 :)  
https://docs.unity3d.com/ScriptReference/  
# 筆記 Input.GetAxis(string axisName)  
axisName有哪些我其實也不知道,但是可以到Input Manager中進行修正或修改  
常用的有四個"Vertical","Horizontal","Mouse X","Mouse Y"  
"Vertical"   偵測鍵盤W和S/up和down(-1,0,1)  
"Horizontal" 偵測鍵盤A和D/right和left(-1,0,1)  
"Mouse X"    偵測滑鼠在屏幕X方向之標準化位移量  
"Mouse Y"    偵測滑鼠在屏幕Y方向之標準化位移量    
# 筆記 Quaternion  
Quaternion.LookRotation(Vector3 a,Vector3 b)  
將兩個向量a和b做外積後回傳 *註解如果之輸入一個Vector3 則將Vecter3 b默認為世界的y軸  
Quaternion.Angle(Quaternion a, Quaternion b)  
輸入兩個四元數後回傳兩者之夾角  
Quaternion.Euler(float x, float y, float z)  
輸入三個角度,將尤拉角轉換為四元數  
Quaternion.Slerp(Quaternion a, Quaternion b, float t)  
在四元數a和b之間線性值一個新的四元數  
Quaternion.FromToRotation (Vector3 fromDirection, Vector3 toDirection)  
創建一個rotation 從fromDirection到toDirection  
Quaternion.identity  
這個四元數對應於“無變換”  
剩下不常用所以就懶得翻譯,以下提供連結自行查看    
https://docs.unity3d.com/ScriptReference/Quaternion.html  
