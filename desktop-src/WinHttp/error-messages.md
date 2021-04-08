---
description: 當其中一個 Microsoft Windows HTTP 服務 (WinHTTP) 函式失敗時，此主題中所識別的錯誤值會由 GetLastError 傳回。
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: " (WinHTTP. h) 的錯誤訊息"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850116"
---
# <a name="error-messages-winhttph"></a> (WinHTTP. h) 的錯誤訊息

當其中一個 Microsoft Windows HTTP 服務 (WinHTTP) 函式失敗時， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回下列錯誤值，且在 [**HRESULT**](../com/structure-of-com-error-codes.md) 錯誤的較低16位中也會傳回 [**WinHttpRequest**](winhttprequest.md) 物件。

名稱開頭為 "ERROR \_ WINHTTP \_ " 的錯誤值是 WINHTTP 函式特有的。 在適當的情況下，WinHTTP 函數也會傳回 Windows 錯誤訊息。

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**錯誤 \_ WINHTTP \_ 自動 \_ PROXY \_ 服務 \_ 錯誤**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



當找不到指定 URL 的 proxy 時， [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 會傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**錯誤 \_ WINHTTP 自動偵測 \_ \_ 失敗**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



如果 WinHTTP 無法探索 Proxy 自動設定 (PAC) 檔的 URL，則會傳回 [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**錯誤 \_ WINHTTP 錯誤的 \_ \_ 自動 \_ PROXY \_ 腳本**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



在 Proxy 自動設定 (PAC) 檔中執行腳本時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**\_ \_ \_ \_ 在開啟之後，WINHTTP 無法呼叫錯誤 \_**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



如果在呼叫 [**Open**](iwinhttprequest-open.md)方法之後無法要求指定的選項， [**HttpRequest**](winhttprequest.md)物件會傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**錯誤 \_ WINHTTP \_ 無法 \_ \_ 在傳送後呼叫 \_**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



如果在呼叫 [**Send**](iwinhttprequest-send.md)方法之後無法執行要求的作業， [**HttpRequest**](winhttprequest.md)物件會傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**錯誤 \_ WINHTTP \_ 無法 \_ \_ 在開啟之前呼叫 \_**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



如果在呼叫 [**Open**](iwinhttprequest-open.md)方法之前無法執行要求的作業， [**HttpRequest**](winhttprequest.md)物件會傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**錯誤 \_ WINHTTP \_ 無法 \_ \_ 在傳送前呼叫 \_**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



如果在呼叫 [**傳送**](iwinhttprequest-send.md)方法之前無法執行要求的作業，則由 [**HttpRequest**](winhttprequest.md)物件傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**錯誤 \_ WINHTTP \_ 無法 \_ 連接**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



如果與伺服器的連接失敗，則傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**\_需要 WINHTTP \_ 客戶 \_ 端 \_ 驗證 \_ 憑證錯誤**
</dt> <dd> <dl> <dt>



伺服器需要 SSL 用戶端驗證。 應用程式會使用 **WINHTTP \_ 選項 [ \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單**] 選項來呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ，以抓取憑證簽發者的清單。 如需詳細資訊，請參閱 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項。

如果伺服器要求用戶端憑證，但不需要它，應用程式可以使用 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容** 選項來呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。 在此情況下，應用程式會 \_ \_ \_ \_ 在 **WinHttpSetOption** 的 *lpBuffer* 參數中指定 WINHTTP NO CLIENT CERT CONTEXT 宏。 如需詳細資訊，請參閱 **WINHTTP \_ option \_ CLIENT \_ CERT \_ CONTEXT** 選項。

**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 不支援此錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**錯誤 \_ WINHTTP \_ 用戶端憑證 \_ \_ 無 \_ 存取 \_ 私密金鑰 \_**
</dt> <dd> <dl> <dt>



應用程式沒有存取與用戶端憑證相關聯之私密金鑰的必要許可權。

**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 不支援此錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**錯誤 \_ WINHTTP \_ 用戶端憑證 \_ \_ 沒有 \_ 私密金鑰 \_**
</dt> <dd> <dl> <dt>



SSL 用戶端憑證的內容沒有相關聯的私密金鑰。 用戶端憑證可能已匯入沒有私密金鑰的電腦。

**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 不支援此錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**錯誤 \_ WINHTTP \_ 區塊 \_ 編碼 \_ 標頭 \_ 大小 \_ 溢位**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



當剖析區塊編碼過程中發生溢位狀況時，由 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**\_需要 WINHTTP \_ 客戶 \_ 端 \_ 驗證 \_ 憑證錯誤**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



當伺服器要求用戶端驗證時， [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 會傳回。

**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 不支援此錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**發生錯誤 \_ WINHTTP \_ 連接 \_ 錯誤**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



與伺服器的連接已重設或終止，或遇到不相容的 SSL 通訊協定。 例如，除非用戶端明確啟用，否則 WinHTTP 5.1 版不支援 SSL2。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**錯誤 \_ WINHTTP \_ 標頭 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



目前不再使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**超過錯誤的 \_ WINHTTP \_ 標頭 \_ 計數 \_**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



當回應中出現的標頭數目超過 WinHTTP 可能接收的標頭數目時， [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 會傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**\_ \_ \_ \_ 找不到錯誤的 WINHTTP 標頭**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



找不到要求的標頭。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**錯誤 \_ WINHTTP \_ 標頭 \_ 大小 \_ 溢位**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



當收到的標頭大小超過要求控制碼的限制時，由 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**錯誤 \_ WINHTTP 錯誤的 \_ \_ 處理 \_ 狀態**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



因為提供的控制碼不是正確的狀態，所以無法執行要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**錯誤 \_ WINHTTP 錯誤的 \_ \_ 控制碼 \_ 類型**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



提供的控制碼類型對這項作業而言不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**錯誤 \_ WINHTTP \_ 內部 \_ 錯誤**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



發生內部錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**錯誤 \_ WINHTTP \_ 無效 \_ 選項**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



要求 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 指定了不正確選項值。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**錯誤 \_ WINHTTP \_ 不正確 \_ 查詢 \_ 要求**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



目前不再使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**錯誤 \_ WINHTTP \_ 不正確 \_ 伺服器 \_ 回應**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



無法剖析伺服器回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**錯誤 \_ WINHTTP \_ 不正確 \_ URL**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



URL 無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**錯誤 \_ WINHTTP \_ 登入 \_ 失敗**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



登入嘗試失敗。 當遇到此錯誤時，應使用 [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)來關閉要求控制碼。 必須先建立新的要求控制碼，才能重試原本產生此錯誤的函式。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**錯誤 \_ WINHTTP \_ 名稱 \_ 未 \_ 解決**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



無法解析伺服器名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**錯誤 \_ WINHTTP \_ 未 \_ 初始化**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



目前不再使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**\_WINHTTP \_ 操作已 \_ 取消時發生錯誤**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



作業已取消，通常是因為要求操作的控制碼已在作業完成之前關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**\_ \_ \_ 無法設定錯誤 WINHTTP \_ 選項**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



無法設定所要求的選項，只能進行查詢。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**\_WINHTTP \_ 超出 \_ \_ 控制碼錯誤**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



目前不再使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**錯誤 \_ WINHTTP 重新 \_ 導向 \_ 失敗**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



重新導向失敗，因為配置變更或嘗試重新導向失敗 (預設為五次嘗試) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**\_WINHTTP \_ 重新傳送 \_ 要求時發生錯誤**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



WinHTTP 函數失敗。 您可以在相同的要求控制碼上重試所需的函數。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**錯誤 \_ WINHTTP \_ 回應 \_ 清空 \_ 溢位**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



當傳入回應超過內部 WinHTTP 大小限制時傳回。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**錯誤 \_ WINHTTP \_ 腳本 \_ 執行 \_ 錯誤**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



執行腳本時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**錯誤 \_ WINHTTP \_ 安全 \_ CERT \_ CN \_ 無效**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



當憑證 CN 名稱不符合傳遞的值時傳回 (相當於 **CERT \_ E \_ CN \_ NO \_ match** error) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 憑證 \_ 日期 \_ 無效**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



指出當確認憑證中的目前系統時鐘或時間戳記時，所需的憑證不在有效期間內，或是憑證鏈的有效期間未正確地 (等於 **cert \_ e 已 \_ 過期** 或 **cert \_ e \_ VALIDITYPERIODNESTING** 錯誤) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**錯誤 \_ WINHTTP \_ 安全 \_ CERT \_ REV \_ 失敗**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



表示無法檢查撤銷，因為撤銷伺服器已離線 (相當於 **\_ \_ \_ 離線 CRYPT E 撤銷**) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**錯誤 \_ WINHTTP \_ 安全憑證已 \_ \_ 撤銷**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



表示已撤銷憑證 (相當於 **CRYPT \_ E \_ 撤銷** 的) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 憑證 \_ 錯誤的 \_ 使用方式**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



指出憑證對要求的使用方式無效 (等同于 **CERT \_ E \_ 錯誤的 \_ 使用** 方式) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 通道 \_ 錯誤**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



指出與安全通道有關的錯誤 (與以 "SEC \_ E \_ " 和 "sec I" 開頭的錯誤碼相同 \_ \_) 的 "winerror.h .h" 標頭檔中。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 失敗**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



伺服器傳送的安全通訊端層 (SSL) 憑證中找到一或多個錯誤。 若要判斷所遇到的錯誤類型，請檢查狀態回呼函式中的 [**WINHTTP \_ 回呼 \_ 狀態 \_ 安全 \_ 失敗**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 通知。 如需詳細資訊，請參閱 [**WINHTTP \_ 狀態 \_ 回呼**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 不正確 \_ CA**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



指出已處理憑證鏈，但在信任提供者不信任的根憑證中終止 (等同于 **CERT \_ E \_ UNTRUSTEDROOT**) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 無效 \_ 的憑證**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



指出憑證無效 (等同于 **cert \_ e \_ 角色**、 **cert \_ e \_ PATHLENCONST**、 **cert \_ e \_ CRITICAL**、 **Cert \_ e \_ 用途**、 **cert \_ e \_ ISSUERCHAINING**、 **cert \_ e \_ 格式錯誤** 和 **cert \_ e \_ 鏈**) 等錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**\_WINHTTP \_ 關機錯誤**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



正在關閉或卸載 WinHTTP 函數支援。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**錯誤 \_ WINHTTP \_ 超時**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



要求已逾時。

無論在 Windows HTTP 服務中設定的超時值為何，都可能會因為 TCP/IP 超時行為而傳回此錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**錯誤 \_ WINHTTP \_ 無法 \_ \_ 下載 \_ 腳本**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



無法下載 PAC 檔案。 例如，PAC URL 所參考的伺服器可能無法連線，或伺服器傳回404找不到的回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**錯誤 \_ WINHTTP \_ 未處理的 \_ 腳本 \_ 類型**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



不支援腳本類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**錯誤 \_ WINHTTP \_ 無法辨識的 \_ 配置**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



URL 指定了 "HTTP：" 或 "HTTPs：" 以外的配置。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**
</dt> <dd> <dl> <dt>



可用的記憶體不足，無法完成要求的操作。

**標頭：** 在 Winerror.h 中宣告


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**\_緩衝區不足的錯誤 \_**
</dt> <dd> <dl> <dt>



提供給函數的緩衝區大小（以位元組為單位）不足以包含傳回的資料。 如需詳細資訊，請參閱特定功能。

**標頭：** 在 Winerror.h 中宣告


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**錯誤 \_ 不正確 \_ 控制碼**
</dt> <dd> <dl> <dt>



傳遞至應用程式設計介面 (API) 的控制碼已失效或已關閉。

**標頭：** 在 Winerror.h 中宣告


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**錯誤 \_ 的 \_ 檔案 \_**
</dt> <dd> <dl> <dt>



找不到其他檔案。

**標頭：** 在 Winerror.h 中宣告


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_沒有 \_ 其他 \_ 專案的錯誤**
</dt> <dd> <dl> <dt>



找不到更多專案。

**標頭：** 在 Winerror.h 中宣告


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**\_不 \_ 支援的錯誤**
</dt> <dd> <dl> <dt>



未載入所需的通訊協定堆疊，且應用程式無法啟動 WinSock。

**標頭：** 在 Winerror.h 中宣告


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| 標頭<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

