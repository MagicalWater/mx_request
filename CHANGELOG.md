## 1.0.5
- 修正因合併資料導致舊資料重複出現的問題, 調整option與requestContent合併參數的方式
- 修正body資料設置失效的問題

## 1.0.4
- 修正當query的value有非字串的資料(例如整數), 就會造成轉化成uri出現錯誤, 因此將query直接丟給dio進行處理, 不再參與構建uri
- mxRequest與mxDownload新增query參數, 可以直接傳入Map<String, dynamic>的參數, 會自動與RequestContent的query合併

## 1.0.3
- 抽離自動生成request內容相關的程式碼到[mx_request_generator](https://pub.dev/packages/mx_request_generator)套件
- 修正當沒有指定contentType時, 會導致body沒有生效的問題

## 1.0.2
- 調整dio extension加入mxDownload, 表明使用下載的方式進行請求
- 調整dio extension原本的connect方法名稱, 變更為mxRequest
- 新增RequestContent擴展, 分別加入request與download, 對應dio的mxRequest與mxDownload

## 1.0.1
- 調整meta套件的版本最小為1.15.0, 與flutter SDK同步

## 1.0.0
- 前身為mx_http, 拋棄HttpUtil, 更改為圍繞的Dio套件的擴展
- 優化自動生成請求的內容
