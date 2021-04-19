---
title: 'HTTP_LOG_FIELD_ 常數 (Http.sys) '
description: 定義 W3C 記錄檔和錯誤記錄檔中的欄位。
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966100"
---
# <a name="http_log_field_-constants"></a>HTTP \_ 記錄 \_ 欄位 \_ 常數

**HTTP \_ 記錄 \_ 欄位 \_** 常數會定義 W3C 記錄檔和錯誤記錄檔中的欄位。

這些常數會在 [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info) 結構中使用。

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP \_ 記錄 \_ 欄位 \_ 日期**
</dt> <dd> <dl> <dt>



活動發生的日期。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP \_ 記錄 \_ 欄位 \_ 時間**
</dt> <dd> <dl> <dt>



發生活動的時間，以國際標準時間 (UTC) 。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP \_ 記錄 \_ 欄位 \_ 用戶端 \_ IP**
</dt> <dd> <dl> <dt>



發出要求之用戶端的 IP 位址。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP \_ 記錄 \_ 欄位 \_ 使用者 \_ 名稱**
</dt> <dd> <dl> <dt>



存取您的伺服器之已驗證使用者的名稱。 匿名使用者會以連字號表示。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP \_ 記錄 \_ 欄位 \_ 網站 \_ 名稱**
</dt> <dd> <dl> <dt>



產生記錄檔專案所在的網站名稱。


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**HTTP \_記錄 \_ 欄位 \_ 電腦 \_ 名稱**
</dt> <dd> <dl> <dt>



產生記錄檔專案所在的電腦名稱稱。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP \_ 記錄 \_ 欄位 \_ 伺服器 \_ IP**
</dt> <dd> <dl> <dt>



產生記錄檔專案之伺服器的 IP 位址。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP \_ 記錄 \_ 欄位 \_ 方法**
</dt> <dd> <dl> <dt>



要求的動作，例如 get 方法。


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**HTTP \_記錄 \_ 欄位 \_ URI \_ 詞幹**
</dt> <dd> <dl> <dt>



動作的目標，例如 Default.htm。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP \_ 記錄 \_ 欄位 \_ URI \_ 查詢**
</dt> <dd> <dl> <dt>



用戶端嘗試執行的查詢（如果有的話）。 只有針對動態頁面才需要執行通用資源識別元 (URI) 查詢。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP \_ 記錄 \_ 欄位 \_ 狀態**
</dt> <dd> <dl> <dt>



HTTP 狀態碼。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP \_ 記錄 \_ 欄位 \_ WIN32 \_ 狀態**
</dt> <dd> <dl> <dt>



Windows 狀態碼。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP \_ 記錄 \_ 欄位 \_ 傳送位元組數 \_**
</dt> <dd> <dl> <dt>



伺服器所傳送的位元組數目（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP \_ 記錄 \_ 欄位 \_ 位元組 \_ 接收**
</dt> <dd> <dl> <dt>



伺服器收到的數位（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**花費的 HTTP \_ 記錄 \_ 欄位 \_ 時間 \_**
</dt> <dd> <dl> <dt>



動作的時間（以毫秒為單位）。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP \_ 記錄 \_ 欄位 \_ 伺服器 \_ 埠**
</dt> <dd> <dl> <dt>



針對服務設定的伺服器埠號碼。


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**HTTP \_記錄 \_ 欄位 \_ 使用者 \_ 代理程式**
</dt> <dd> <dl> <dt>



用戶端使用的應用程式。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP \_ 記錄 \_ 欄位 \_ COOKIE**
</dt> <dd> <dl> <dt>



傳送或接收的 cookie 內容（如果有的話）。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP \_ 記錄 \_ 欄位 \_ 推薦者**
</dt> <dd> <dl> <dt>



使用者上次造訪的網站。 這個網站提供目前網站的連結。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP \_ 記錄 \_ 欄位 \_ 版本**
</dt> <dd> <dl> <dt>



用戶端使用的 HTTP 通訊協定版本。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP \_ 記錄 \_ 欄位 \_ 主機**
</dt> <dd> <dl> <dt>



主機標頭名稱（如果有的話）。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP \_ 記錄 \_ 欄位 \_ 子 \_ 狀態**
</dt> <dd> <dl> <dt>



子狀態錯誤碼。


</dt> </dl> </dd> </dl>

下列常數用於 HTTP 錯誤記錄。

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP \_ 記錄 \_ 欄位 \_ 用戶端 \_ 埠**
</dt> <dd> <dl> <dt>



接收要求的用戶端埠號碼。 此記錄欄位只會用於錯誤記錄。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP \_ 記錄 \_ 欄位 \_ URI**
</dt> <dd> <dl> <dt>



要求中收到的 URI，包括查詢部分。 此記錄欄位只會用於錯誤記錄。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP \_ 記錄 \_ 欄位 \_ 網站 \_ 識別碼**
</dt> <dd> <dl> <dt>



路由要求的 URL 群組之應用程式特定的數值識別碼。 此記錄欄位只會用於錯誤記錄。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP \_ 記錄 \_ 欄位 \_ 原因**
</dt> <dd> <dl> <dt>



錯誤原因片語。 此記錄欄位只會用於錯誤記錄。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP \_ 記錄 \_ 欄位 \_ 佇列 \_ 名稱**
</dt> <dd> <dl> <dt>



分派要求的要求佇列名稱。 此記錄欄位只會用於錯誤記錄。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP \_ 記錄 \_ 欄位 \_ STREAMID**
</dt> <dd> <dl> <dt>



資料流程識別碼。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Http.sys</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[HTTP 伺服器 API 版本2.0 常數](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





