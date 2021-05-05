## PowerBI 貓空載運量數據分析

*以下為視覺化分析所使用的資料及清理資料分析遇到的問體

*使用資料集：

臺北市貓空纜車各站進出人次-臺北市交通統計查詢系統
http://dotstat.taipei.gov.tw/pxweb2007P/Dialog/varval.asp?ma=TP10402M&ti=%BBO%A5%5F%A5%AB%BF%DF%AA%C5%C6l%A8%AE%A6U%AF%B8%B6i%A5X%A4H%A6%B8&path=../PXfile/CountyStatistics&lang=9&strList=L

臺北市立動物園歷年人數統計-臺北市立動物園
https://www.zoo.gov.taipei/News_Content.aspx?n=185FCFADA1FEA0F7&sms=922BAE075F221DD4&s=BA3C2B1925FB8942

每日貓空纜車系統旅運量統計表-政府資料開放平臺
https://data.gov.tw/dataset/61793

 貓空纜車團體預約統計資料
https://data.gov.tw/dataset/61846整理資料時是否有遭遇哪些問題
  
整合匯進70個csv資料檔於一個excel
解決方法：利用命令提示字元合併多個csv檔
先把要所有要合併的csv檔放在同一個資料夾，之後再輸入指令碼，就有合併完成了。


*問題解決

** 資料格式時間不一
解決方法：使用excel取代功能並刪除空白資料

** 進行兩個不同資料的插入欄位
解決方法：使用vlookup功能選取插入，但礙於有些資料的沒有對應數值且在大筆資料下會造成你一次動作往下拉會使數字重複，於是改用星期去合併彙算

** 以為資料完整-解果發現東缺西缺
解決方法：用平均Average去計算

** 兩者資料關聯性的正確性
解決方法：需要更細節的數據去計算進入動物園並有搭乘貓空的人數，因為台北市政府的開放資料是算總貓空載運量，並沒有再細分各進站出站的人數資料，因此就要再去交通處資料找在動物園進站和出站的人數，才能真正去分析兩者真正的關聯性。
