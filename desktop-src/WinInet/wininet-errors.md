---
title: " (Wininet. h) 的錯誤訊息"
description: WinINet 函數會在適當的情況下傳回錯誤碼。 下列是 WinINet 函數特有的錯誤。
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106458"
---
# <a name="error-messages-winineth"></a> (Wininet. h) 的錯誤訊息

WinINet 函數會在適當的情況下傳回錯誤碼。 下列是 WinINet 函數特有的錯誤。

<dl> <dt>

<span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**錯誤 \_ FTP \_ 中斷**
</dt> <dd> <dl> <dt>

12111
</dt> <dt>



FTP 作業未完成，因為會話已中止。


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**錯誤 \_ FTP \_ 無 \_ 被動 \_ 模式**
</dt> <dd> <dl> <dt>

12112
</dt> <dt>



被動模式無法在伺服器上使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**\_FTP \_ 傳輸 \_ 進行中 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

12110
</dt> <dt>



無法在 FTP 會話控制碼上進行要求的作業，因為操作已在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 GOPHER 屬性**
</dt> <dd> <dl> <dt>

12137
</dt> <dt>



找不到要求的屬性。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**錯誤 \_ GOPHER \_ 資料 \_ 錯誤**
</dt> <dd> <dl> <dt>

12132
</dt> <dt>



從 Gopher 伺服器接收資料時，偵測到錯誤。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**錯誤 \_ GOPHER \_ \_ 資料結尾 \_**
</dt> <dd> <dl> <dt>

12133
</dt> <dt>



已到達資料的結尾。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**錯誤 \_ GOPHER \_ 不正確的 \_ 定位器 \_ 類型**
</dt> <dd> <dl> <dt>

12135
</dt> <dt>



此操作的定位器類型不正確。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**錯誤 \_ GOPHER \_ 無效 \_ 定位器**
</dt> <dd> <dl> <dt>

12134
</dt> <dt>



提供的定位器無效。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**錯誤 \_ GOPHER \_ 非 \_ 檔案**
</dt> <dd> <dl> <dt>

12131
</dt> <dt>



您必須對檔案定位器提出要求。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**錯誤 \_ GOPHER \_ 未 \_ GOPHER \_ 加號**
</dt> <dd> <dl> <dt>

12136
</dt> <dt>



要求的作業只能針對 Gopher + 伺服器，或使用指定 Gopher + 作業的定位器進行。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**錯誤 \_ GOPHER \_ 通訊協定 \_ 錯誤**
</dt> <dd> <dl> <dt>

12130
</dt> <dt>



剖析從 Gopher 伺服器傳回的資料時，偵測到錯誤。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**錯誤 \_ GOPHER \_ 未知 \_ 定位器**
</dt> <dd> <dl> <dt>

12138
</dt> <dt>



定位器類型未知。

> [!Note]  
> 僅限 windows XP 及 Windows Server 2003 R2 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**\_拒絕 HTTP \_ COOKIE \_ 錯誤**
</dt> <dd> <dl> <dt>

12162
</dt> <dt>



伺服器拒絕了 HTTP cookie。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**錯誤 \_ HTTP \_ COOKIE \_ 需要 \_ 確認**
</dt> <dd> <dl> <dt>

12161
</dt> <dt>



HTTP cookie 需要確認。

> [!Note]  
> Windows Vista 和 Windows Server 2008 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**\_HTTP \_ 下層 \_ 伺服器錯誤**
</dt> <dd> <dl> <dt>

12151
</dt> <dt>



伺服器未傳回任何標頭。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**錯誤 \_ HTTP \_ 標頭 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



無法新增標頭，因為它已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_ \_ \_ 找不到 HTTP 標頭 \_ 錯誤**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



找不到要求的標頭。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**錯誤 \_ HTTP \_ 無效 \_ 標頭**
</dt> <dd> <dl> <dt>

12153
</dt> <dt>



提供的標頭無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**\_HTTP \_ 無效 \_ 查詢 \_ 要求錯誤**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



對 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 提出的要求無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**錯誤 \_ HTTP \_ 不正確 \_ 伺服器 \_ 回應**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



無法剖析伺服器回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**錯誤 \_ HTTP \_ 未重新 \_ 導向**
</dt> <dd> <dl> <dt>

12160
</dt> <dt>



未重新導向 HTTP 要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**錯誤 \_ HTTP 重新 \_ 導向 \_ 失敗**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



重新導向失敗，因為配置變更 (例如，將 HTTP 變更為 FTP) 或嘗試重新導向失敗 (預設為五次嘗試) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**錯誤 \_ HTTP 重新 \_ 導向 \_ 需要 \_ 確認**
</dt> <dd> <dl> <dt>

12168
</dt> <dt>



重新導向需要使用者確認。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**錯誤 \_ 網際網路 \_ 非同步 \_ 執行緒 \_ 失敗**
</dt> <dd> <dl> <dt>

12047
</dt> <dt>



應用程式無法啟動非同步執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**錯誤 \_ 網際網路 \_ 錯誤 \_ 自動 \_ PROXY \_ 腳本**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



自動 proxy 設定腳本中發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**\_網際網路錯誤 \_ \_ 選項 \_ 長度錯誤**
</dt> <dd> <dl> <dt>

12010
</dt> <dt>



針對指定的選項類型，提供給 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 或 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 之選項的長度不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**網際網路錯誤的登錄 \_ \_ \_ \_ 參數錯誤**
</dt> <dd> <dl> <dt>

12022
</dt> <dt>



找不到必要的登錄值，但是不正確的類型或具有不正確值。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**\_網際網路 \_ 無法 \_ 連接時發生錯誤**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



嘗試連接到伺服器失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**\_INTERNET \_ CHG \_ POST \_ 不 \_ \_ 安全的錯誤**
</dt> <dd> <dl> <dt>

12042
</dt> <dt>



應用程式正在張貼，並且嘗試在不安全的伺服器上變更多行文字。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**\_需要網際網路 \_ 客戶 \_ 端 \_ 驗證 \_ 憑證時發生錯誤**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



伺服器正在要求用戶端驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**\_ \_ \_ \_ 未設定網際網路用戶端驗證時發生錯誤 \_**
</dt> <dd> <dl> <dt>

12046
</dt> <dt>



未在這部電腦上設定用戶端授權。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**\_網際網路 \_ 連接已 \_ 中止時發生錯誤**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



與伺服器的連接已終止。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**\_網際網路 \_ 連接 \_ 重設時發生錯誤**
</dt> <dd> <dl> <dt>

12031
</dt> <dt>



與伺服器的連接已重設。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**錯誤 \_ 網際網路 \_ 解碼 \_ 失敗**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



WinINet 無法對回應執行內容解碼。 如需詳細資訊，請參閱 [**內容編碼**](content-encoding.md) 主題。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**錯誤 \_ 網際網路 \_ 對話方塊 \_ 暫止**
</dt> <dd> <dl> <dt>

12049
</dt> <dt>



另一個執行緒正在進行密碼對話方塊。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**\_網際網路中斷連線時發生錯誤 \_**
</dt> <dd> <dl> <dt>

12163
</dt> <dt>



網際網路連線已中斷。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**\_網際網路 \_ 擴充 \_ 錯誤時發生錯誤**
</dt> <dd> <dl> <dt>

12003
</dt> <dt>



從伺服器傳回了擴充錯誤。 這通常是包含詳細錯誤訊息的字串或緩衝區。 呼叫 [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) 以取得錯誤文字。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**\_網際網路 \_ 失敗 \_ DUETOSECURITYCHECK 時發生錯誤**
</dt> <dd> <dl> <dt>

12171
</dt> <dt>



因為有安全性檢查，所以函數失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**\_網際網路 \_ 強制 \_ 重試時發生錯誤**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



函數需要重做要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**\_需要的網際網路 \_ FORTEZZA \_ 登 \_ 入錯誤**
</dt> <dd> <dl> <dt>

12054
</dt> <dt>



要求的資源需要 Fortezza 驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**\_網際網路 \_ 控制碼 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

12036
</dt> <dt>



要求失敗，因為控制碼已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**\_ \_ \_ \_ \_ REDIR 上的網際網路 HTTP 至 \_ HTTPS 時發生錯誤**
</dt> <dd> <dl> <dt>

12039
</dt> <dt>



由於有重新導向，因此應用程式會從非 SSL 連線到 SSL 連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**\_網際網路 \_ HTTPS \_ HTTP \_ 提交 \_ REDIR 時發生錯誤**
</dt> <dd> <dl> <dt>

12052
</dt> <dt>



提交至 SSL 連線的資料會被重新導向至非 SSL 連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**\_ \_ \_ \_ \_ REDIR 上的網際網路 HTTPS 與 \_ HTTP 時發生錯誤**
</dt> <dd> <dl> <dt>

12040
</dt> <dt>



由於有重新導向，因此應用程式會從 SSL 移至非 SSL 連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**\_網際網路 \_ 格式不正確 \_ 的錯誤**
</dt> <dd> <dl> <dt>

12027
</dt> <dt>



要求的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**錯誤的 \_ 網際網路錯誤 \_ \_ 處理 \_ 狀態**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



因為提供的控制碼不是正確的狀態，所以無法執行要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**\_網際網路 \_ 不正確的 \_ 控制碼 \_ 類型錯誤**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



提供的控制碼類型對這項作業而言不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**錯誤的 \_ 網際網路錯誤 \_ \_ 密碼**
</dt> <dd> <dl> <dt>

12014
</dt> <dt>



無法完成連接和登入 FTP 伺服器的要求，因為提供的密碼不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**錯誤 \_ 網際網路 \_ 不正確的 \_ 使用者 \_ 名稱**
</dt> <dd> <dl> <dt>

12013
</dt> <dt>



無法完成連接和登入 FTP 伺服器的要求，因為提供的使用者名稱不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**\_網際網路 \_ 插入 \_ CDROM 時發生錯誤**
</dt> <dd> <dl> <dt>

12053
</dt> <dt>



要求需要將 CD-ROM 插入 cd-rom 光碟機，以找出所要求的資源。

> [!Note]  
> Windows Vista 和 Windows Server 2008 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**\_網際網路 \_ 內部 \_ 錯誤時發生錯誤**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



發生內部錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**\_網際網路 \_ 不正確 \_ CA 錯誤**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



此函數不熟悉產生伺服器憑證的憑證授權單位單位。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**\_網際網路 \_ 無效 \_ 操作時發生錯誤**
</dt> <dd> <dl> <dt>

12016
</dt> <dt>



要求的作業無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**\_網際網路 \_ 無效 \_ 選項時發生錯誤**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



要求 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 或 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 指定了不正確選項值。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**\_網際網路 \_ 不正確 \_ PROXY \_ 要求時發生錯誤**
</dt> <dd> <dl> <dt>

12033
</dt> <dt>



對 proxy 的要求無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**\_網際網路 \_ 不正確 \_ URL 錯誤**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



URL 無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**\_ \_ \_ 找不到網際網路 \_ 專案錯誤**
</dt> <dd> <dl> <dt>

12028
</dt> <dt>



找不到要求的專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**\_網際網路 \_ 登入 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



連接和登入 FTP 伺服器的要求失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**\_網際網路 \_ 登入 \_ 失敗 \_ 顯示 \_ 實體 \_ 主體時發生錯誤**
</dt> <dd> <dl> <dt>

12174
</dt> <dt>



已從網站傳回 MS-Logoff 摘要標頭。 此標頭會明確指示摘要套件清除相關領域的認證。 只有在已設定 [網際網路 \_ 錯誤 \_ 遮罩 \_ 登入 \_ 失敗 \_ 顯示 \_ 實體 \_](option-flags.md) 內容選項時，才會傳回此錯誤; 否則會傳回 **錯誤 \_ 網際網路登入 \_ \_ 失敗** 。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**\_網際網路 \_ 混合 \_ 安全性錯誤**
</dt> <dd> <dl> <dt>

12041
</dt> <dt>



內容並不完全安全。 某些正在觀看的內容可能來自不安全的伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**錯誤 \_ 網際網路 \_ 名稱 \_ 未 \_ 解決**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



無法解析伺服器名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**\_網際網路 \_ 需要 \_ MSN \_ SSPI \_ PKG 時發生錯誤**
</dt> <dd> <dl> <dt>

12173
</dt> <dt>



目前未實作。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**\_網際網路 \_ 需要 \_ UI 時發生錯誤**
</dt> <dd> <dl> <dt>

12034
</dt> <dt>



已要求使用者介面或其他封鎖作業。

> [!Note]  
> Windows Vista 和 Windows Server 2008 及更早版本。

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**錯誤 \_ 網際網路 \_ 沒有 \_ 回呼**
</dt> <dd> <dl> <dt>

12025
</dt> <dt>



因為尚未設定回呼函式，所以無法進行非同步要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**錯誤 \_ 網際網路 \_ 沒有 \_ 內容**
</dt> <dd> <dl> <dt>

12024
</dt> <dt>



因為提供了零內容值，所以無法進行非同步要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**錯誤 \_ 網際網路 \_ 沒有 \_ 直接 \_ 存取**
</dt> <dd> <dl> <dt>

12023
</dt> <dt>



目前無法進行直接網路存取。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**\_ \_ 未初始化網際網路 \_ 錯誤**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



尚未初始化 WinINet API。 指出尚未呼叫較高層級的函式，例如 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**\_網際網路 \_ 不是 \_ PROXY \_ 要求時發生錯誤**
</dt> <dd> <dl> <dt>

12020
</dt> <dt>



無法透過 proxy 提出要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**錯誤 \_ 網際網路 \_ 操作已 \_ 取消**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



作業已取消，通常是因為要求操作的控制碼已在作業完成之前關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**\_ \_ \_ 無法設定錯誤網際網路 \_ 選項**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



無法設定所要求的選項，只能進行查詢。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**\_網際網路 \_ \_ 的 \_ 控制碼錯誤**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



目前無法產生更多的控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**錯誤 \_ 網際網路 \_ POST \_ 為 \_ 非 \_ 安全的**
</dt> <dd> <dl> <dt>

12043
</dt> <dt>



應用程式正在將資料張貼至不安全的伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**\_ \_ \_ 找不到網際網路通訊協定 \_ 錯誤**
</dt> <dd> <dl> <dt>

12008
</dt> <dt>



找不到要求的通訊協定。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**\_無法連線到網際網路 \_ PROXY \_ 伺服器 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

12165
</dt> <dt>



無法連線到指定的 proxy 伺服器。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**錯誤 \_ 網際網路重新 \_ 導向 \_ 配置 \_ 變更**
</dt> <dd> <dl> <dt>

12048
</dt> <dt>



函數無法處理重新導向，因為配置 (例如，將 HTTP 變更為 FTP) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**\_ \_ \_ \_ \_ 找不到網際網路登錄值錯誤**
</dt> <dd> <dl> <dt>

12021
</dt> <dt>



找不到必要的登錄值。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**\_網際網路 \_ 要求 \_ 暫止時發生錯誤**
</dt> <dd> <dl> <dt>

12026
</dt> <dt>



因為有一或多個要求暫止，所以無法完成所需的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**\_網際網路 \_ 重試 \_ 對話方塊時發生錯誤**
</dt> <dd> <dl> <dt>

12050
</dt> <dt>



對話方塊應該會重試。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**\_INTERNET \_ SEC \_ CERT \_ CN \_ 不正確錯誤**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



SSL 憑證一般名稱 (主控制項名稱欄位) 不正確，例如，如果您輸入 www.server.com，而憑證上的一般名稱顯示為 www.different.com。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**錯誤 \_ 網際網路 \_ SEC \_ 憑證 \_ 日期 \_ 無效**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



從伺服器收到的 SSL 憑證日期不正確。 憑證已過期。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**\_INTERNET \_ SEC \_ CERT \_ 錯誤**
</dt> <dd> <dl> <dt>

12055
</dt> <dt>



SSL 憑證包含錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**錯誤 \_ 網際網路 \_ SEC \_ CERT \_ 沒有 \_ REV**
</dt> <dd> <dl> <dt>

12056
</dt> <dt>



SSL 憑證未撤銷。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**\_INTERNET \_ SEC \_ CERT \_ REV \_ 失敗的錯誤**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



撤銷 SSL 憑證失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**\_INTERNET \_ SEC CERT \_ 已 \_ 撤銷的錯誤**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



SSL 憑證已撤銷。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**錯誤 \_ 網際網路 \_ SEC \_ 無效 \_ 的憑證**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



SSL 憑證無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**錯誤 \_ 網際網路 \_ 安全性 \_ 通道 \_ 錯誤**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



應用程式在載入 SSL 程式庫時遇到內部錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**\_網際網路 \_ 伺服器 \_ 無法連線時發生錯誤**
</dt> <dd> <dl> <dt>

12164
</dt> <dt>



指定的網站或伺服器無法連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**\_網際網路 \_ 關機時發生錯誤**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



WinINet 支援即將關閉或卸載。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**\_ \_ \_ 未安裝網際網路 TCPIP \_ 的錯誤**
</dt> <dd> <dl> <dt>

12159
</dt> <dt>



未載入所需的通訊協定堆疊，且應用程式無法啟動 WinSock。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**錯誤 \_ 網際網路 \_ 超時**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



要求已逾時。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**\_網際網路 \_ 無法 \_ \_ 緩存 \_ 檔時發生錯誤**
</dt> <dd> <dl> <dt>

12158
</dt> <dt>



函數無法快取該檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**\_網際網路 \_ 無法 \_ \_ 下載 \_ 腳本時發生錯誤**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



無法下載自動 proxy 設定腳本。 網際網路 \_ 旗標 \_ 必須設定快取 \_ \_ 要求旗標。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**\_網際網路 \_ 無法辨識的 \_ 配置時發生錯誤**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



無法辨識或不支援 URL 配置。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**錯誤 \_ 不正確 \_ 控制碼**
</dt> <dd> <dl> <dt>



傳遞至 API 的控制碼已無效或已關閉。

**標頭：** 在 Winerror.h 中宣告


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**錯誤 \_ 的 \_ 資料**
</dt> <dd> <dl> <dt>



有更多可用的資料。

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


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wininet</dt> </dl> |



 

