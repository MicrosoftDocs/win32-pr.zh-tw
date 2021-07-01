---
title: W3C 記錄
description: W3C 擴充記錄是伺服器端記錄類型，可以在伺服器會話或 URL 群組上啟用。
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb53ccf3b6bf5383a0a4da62538b6fa516c500f8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119943"
---
# <a name="w3c-logging"></a>W3C 記錄

W3C 擴充記錄是伺服器端記錄類型，可以在伺服器會話或 URL 群組上啟用。 在 URL 群組上啟用 W3C 記錄時，只會在路由至 URL 群組的要求上執行記錄。 針對設定為啟用 W3C 記錄的每個 URL 群組，都會建立個別的記錄檔。

當伺服器會話上啟用 W3C 記錄功能時，它會以集中式形式記錄伺服器會話下的所有 URL 群組。 伺服器會話中的所有 URL 群組都會保留單一記錄檔。

下表列出 HTTP 伺服器 API 可記錄的欄位。 資料表包含 [**HTTP \_ 記錄 \_ 欄位**](http-log-field--constants.md) 常數的子集。 以下列出的一些欄位是由 HTTP 伺服器 API 在內部自動產生，因此不包含在 [**HTTP \_ 記錄 \_ 欄位 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_fields_data) 結構中。 [顯示為] 資料行包含記錄檔中顯示的文字。 資料表中的資料會依照記錄檔記錄中的出現順序。

未標記為「HTTP 伺服器 API 已產生」的欄位，必須在應用程式的 [**HTTP \_ 記錄 \_ 欄位 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_fields_data) 結構內傳遞。 應用程式可以從傳遞給它的 [**HTTP \_ 要求**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) 結構產生這些欄位。



| 欄位                            | 顯示為      | 描述                                                                                                                                | HTTP \_ 記錄 \_ 欄位 \_ 資料成員 | HTTP \_ 記錄 \_ 欄位常數      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| 日期                             | date            | 活動發生的日期。                                                                                                   | 已產生 HTTP 伺服器 API。     | HTTP \_ 記錄 \_ 欄位 \_ 日期           |
| 時間                             | time            | 發生活動的時間，以國際標準時間 (UTC) 。                                                             | 已產生 HTTP 伺服器 API。     | HTTP \_ 記錄 \_ 欄位 \_ 時間           |
| 服務名稱和實例號碼 | s-sitename      | 用戶端上執行的網際網路服務名稱和實例編號。                                                              | ServiceName                    | HTTP \_ 記錄 \_ 欄位 \_ 網站 \_ 名稱     |
| Server Name (伺服器名稱)                      | s-computername  | 產生記錄檔專案的伺服器名稱。                                                                          | ServerName                     | HTTP \_ 記錄 \_ 欄位 \_ 電腦 \_ 名稱 |
| 伺服器 IP 位址                | s-ip            | 產生記錄檔專案之伺服器的 IP 位址。                                                                    | ServerIp                       | HTTP \_ 記錄 \_ 欄位 \_ 伺服器 \_ IP     |
| 方法                           | cs 方法       | 要求的動詞，例如 GET 方法。                                                                                             | 方法                         | HTTP \_ 記錄 \_ 欄位 \_ 方法         |
| URI 詞幹                         | cs-uri-詞幹     | 動詞的目標，例如 Default.htm。                                                                                          | UriStem                        | HTTP \_ 記錄 \_ 欄位 \_ URI \_ 詞幹      |
| URI 查詢                        | cs-uri-查詢    | 用戶端嘗試執行的查詢（如果有的話）。 只有針對動態頁面才需要執行通用資源識別元 (URI) 查詢。 | UriQuery                       | HTTP \_ 記錄 \_ 欄位 \_ URI \_ 查詢     |
| 伺服器通訊埠                      | s-埠          | 針對服務設定的伺服器埠號碼。                                                                                 | ServerPort                     | HTTP \_ 記錄 \_ 欄位 \_ 伺服器 \_ 埠   |
| 使用者名稱                        | cs-使用者名稱     | 存取伺服器之已驗證使用者的名稱。 匿名使用者會以連字號表示。                                    | 使用者名稱                       | HTTP \_ 記錄 \_ 欄位 \_ 使用者 \_ 名稱     |
| 用戶端 IP 位址                | c-ip            | 發出要求之用戶端的 IP 位址。                                                                                        | ClientIp                       | HTTP \_ 記錄 \_ 欄位 \_ 用戶端 \_ IP     |
| 通訊協定版本                 | cs-版本      | 用戶端使用的 HTTP 通訊協定版本。                                                                                            | 已產生 HTTP 伺服器 API。     | HTTP \_ 記錄 \_ 欄位 \_ 版本        |
| 使用者代理程式                       | cs (使用者代理程式)   | 用戶端使用的瀏覽器類型。                                                                                                     | UserAgent                      | HTTP \_ 記錄 \_ 欄位 \_ 使用者 \_ 代理程式    |
| Cookie                           | cs (Cookie)       | 傳送或接收的 cookie 內容（如果有的話）。                                                                                        | Cookie                         | HTTP \_ 記錄 \_ 欄位 \_ COOKIE         |
| Referrer                         | cs (查閱者)     | 使用者上次造訪的網站。 這個網站提供目前網站的連結。                                                        | Referrer                       | HTTP \_ 記錄 \_ 欄位查閱者 \_       |
| 主機                             | cs-主機         | 主機標頭名稱（如果有的話）。                                                                                                              | 主機                           | HTTP \_ 記錄 \_ 欄位 \_ 主機           |
| HTTP 狀態                      | sc-狀態       | HTTP 狀態碼。                                                                                                                      | ProtocolStatus                 | HTTP \_ 記錄 \_ 欄位 \_ 狀態         |
| 通訊協定子狀態               | sc-子狀態    | 子狀態錯誤碼。                                                                                                                  | SubStatus                      | HTTP \_ 記錄 \_ 欄位 \_ 子 \_ 狀態    |
| Win32 狀態                     | sc-win32-status | Windows 狀態碼。                                                                                                                   | Win32Status                    | HTTP \_ 記錄 \_ 欄位 \_ WIN32 \_ 狀態  |
| 傳送的位元組數                       | sc-位元組        | 伺服器所傳送的位元組數目。                                                                                                    | 已產生 HTTP 伺服器 API。     | HTTP \_ 記錄 \_ 欄位 \_ 傳送位元組數 \_    |
| 接收的位元組數                   | cs-位元組        | 伺服器所接收和處理的位元組數目。                                                                                  | 已產生 HTTP 伺服器 API。     | HTTP \_ 記錄 \_ 欄位 \_ 位元組 \_ 接收    |
| 花費的時間                       | 花費時間      | 動作所花費的時間長度 (毫秒)。                                                                                  | 已產生 HTTP 伺服器 API。     | 花費的 HTTP \_ 記錄 \_ 欄位 \_ 時間 \_    |
| 串流識別碼                      | streamid          | 資料流程識別碼。                                                                                  | 已產生 HTTP 伺服器 API。     | HTTP \_ 記錄 \_ 欄位 \_ 串流 \_ 識別碼       |



 

記錄檔是可自訂的 ASCII 文字格式。 檔案中的欄位首碼定義如下：

| 前置詞    | 描述                          |
|-----|---------------------------|
| s   | 伺服器動作。           |
| c   | 用戶端動作。           |
| Sc  | 伺服器對用戶端動作。 |
| cs  | 用戶端對伺服器的動作。 |



 

但是，應用程式可以選取一或多個 W3C 擴充記錄檔欄位，但並非所有欄位都包含資訊。 針對已選取但沒有資訊的欄位， ( ) 的連字號會顯示為預留位置。 如果欄位包含非列印字元，HTTP 伺服器 API 會將它取代為加號 (+) ，以保留記錄檔格式。 這通常發生在病毒攻擊的情況下，例如，惡意使用者傳送換行字元和換行字元（如果不是以加號 (+) 取代），就會破壞記錄檔格式。 欄位會以空格分隔。

如果欄位是由 URL 群組或伺服器會話啟用，但未針對要求選取，它就會出現在記錄檔中，並以連字號 ( ) 作為預留位置。

當第一個要求抵達 URL 群組或伺服器會話時，就會建立記錄檔，在設定記錄時，不會建立記錄檔。 下列範例會顯示 W3C 記錄檔的第一個記錄檔專案，其中包含用戶端 IP、使用者名稱、伺服器 IP、伺服器埠、方法、URI 詞幹、URI 查詢、狀態，以及啟用的使用者代理程式欄位：

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

在剖析要求之前，HTTP 伺服器 API 收到第一個位元組時，會初始化所花費的時間欄位。 最後一次傳送完成時，會停止經過時間的時間戳記。 花費的時間不會反映整個網路的時間。 對網站的第一個要求會顯示比其他類似要求更長的時間，因為 HTTP 伺服器 API 會使用第一個要求來開啟記錄檔。

 

 