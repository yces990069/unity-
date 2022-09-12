# unity 學習日誌
2022/3 正式接觸unity 跟著教學做了些有的沒的的小遊戲  
2022/9/5 頹廢整個暑假後開始繼續學  
2022/9/12 學習何謂四元數,嘗試只看unity api做出角色控制器

# 筆記
以下都是我從unityapi抓下來然後解析並白話的翻譯成中文 :)  
# 筆記 Quaternion  
Quaternion.LookRotation(Vector3 a,Vector3 b)  
將兩個向量a和b做外積後回傳 *註解如果之輸入一個Vector3 則將Vecter3 b默認為世界的y軸  
Quaternion.Angle(Quaternion a, Quaternion b)  
輸入兩個四元數後回傳兩者之夾角  
Quaternion.Euler(float x, float y, float z)
輸入三個角度,將尤拉角轉換為四元數
Quaternion.Slerp(Quaternion a, Quaternion b, float t)  
Quaternion.FromToRotation  
and Quaternion.identity  
