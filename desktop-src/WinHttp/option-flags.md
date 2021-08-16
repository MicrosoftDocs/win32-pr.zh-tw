---
Description: WinHttpQueryOption 和 WinHttpSetOption 支援下列選項旗標。
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: '選項旗標 (WinHTTP. h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: ecc3d27bd8d168c276ccac2544dbc648fbdfee5732e87892624903285b3a2fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744059"
---
# <a name="option-flags"></a>選項旗標

[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)和 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)支援下列選項旗標。

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP \_ 選項有 \_ 保證 \_ 非 \_ 封鎖 \_ 回呼**
</dt> <dd> <dl> <dt>



預設值為 FALSE。 如果設定為 TRUE，當用戶端應用程式封鎖狀態回呼時，WinHTTP 無法保證進度。

用戶端應用程式必須特別小心地在回呼內執行最基本的作業，而不會封鎖、儘快傳回，而且特別不能等待任何後續的 WinHTTP 呼叫。 如果未遵循這些指導方針，可能會對效能造成負面影響，或可能應用程式停止回應。 如果以指定的方式使用，此選項可能會改善效能。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP \_ 選項 \_ 自動登入 \_ 原則**
</dt> <dd> <dl> <dt>



設定不帶正負號的長整數值，指定具有下列其中一個值的 [自動登入原則](authentication-in-winhttp.md) 。

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 高 | 未使用預設認證。 請注意，只有當您依實際的電腦名稱稱指定伺服器時，此旗標才會生效。 如果您將伺服器指定為 "localhost" 或 IP 位址，它將不會生效。 |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 低 | 系統會針對所有要求執行使用預設認證的已驗證登入。 |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 中 | 使用預設認證的已驗證登入只會針對近端內部網路上的要求執行。 |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP \_ 選項 \_ 背景 \_ 連接**
</dt> <dd> <dl> <dt>

當您在會話控制碼上設定此選項時，必須傳遞您要開啟的連接數目。 然後，在第一次傳送要求時，WinHttp 會以平行方式開啟多個連接，而不是只開啟單一連線。 這可以改善後續要求對相同目的地的效能，而不會造成連線建立的額外負荷。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP \_ 選項 \_ 回呼**
</dt> <dd> <dl> <dt>



抓取以 [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)設定之回呼函數的指標。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容**
</dt> <dd> <dl> <dt>



設定用戶端憑證內容。 如果應用程式收到 [**\_ \_ \_ \_ \_ 所需的錯誤 WINHTTP 用戶端驗證**](error-messages.md)憑證，則必須先呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 來提供憑證，再重試要求。 在處理此選項的過程中，WinHttp 會在呼叫端提供的憑證內容上呼叫 [**CertDuplicateCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) ，如此一來，呼叫端就可以獨立釋放憑證內容。

> [!Note]
> 應用程式不應該嘗試 \_ \_ 在已從中抓取 \_ \_ 憑證內容的憑證存放區上呼叫 [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) 時，關閉憑證存放區的憑證關閉存放區強制旗標旗標。 可能會發生存取違規。

當伺服器要求用戶端憑證、 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 時，會傳回 [**錯誤 \_ WINHTTP \_ 用戶端 \_ 驗證憑證 \_ \_ 所需**](error-messages.md) 的錯誤。 如果伺服器要求憑證，但不需要憑證，則應用程式可以指定此選項來指出它沒有憑證。 伺服器可以選擇其他驗證配置，或允許匿名存取伺服器。 應用程式會在 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)的 *lpBuffer* 參數中提供 **WINHTTP \_ NO \_ CLIENT \_ CERT \_ CONTEXT** 宏，如下列程式碼範例所示。

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

如果伺服器需要用戶端憑證，它可能會傳送 403 HTTP 狀態碼來回應。 如需詳細資訊，請參閱 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單**
</dt> <dd> <dl> <dt>



當 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)的錯誤是 **\_ \_ \_ \_ \_ 需要的 WINHTTP 用戶端驗證憑證錯誤** 時，會抓取 [**SecPkgCoNtext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)結構。 結構中的簽發者清單包含伺服器 (CA) 可接受的憑證授權單位單位清單。 用戶端應用程式可以篩選 CA 清單，以取得 SSL 驗證的用戶端憑證。

或者，如果伺服器要求用戶端憑證，但不需要它，則應用程式可以使用 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容** 選項來呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。 如需詳細資訊，請參閱 **WINHTTP \_ option \_ CLIENT \_ CERT \_ CONTEXT** 選項。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP \_ 選項 \_ 字碼頁**
</dt> <dd> <dl> <dt>



設定用來處理 URL (也就是查詢字串) 的 [*字碼頁*](glossary.md) 。 預設值為 UTF8。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP \_ 選項 \_ 設定 \_ PASSPORT \_ 驗證**
</dt> <dd> <dl> <dt>



設定不帶正負號的長整數值，這個值會指定是否啟用 [WinHTTP 驗證中的 Passport 驗證](passport-authentication-in-winhttp.md) 。 這個值可以是下列值之一：

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ 停用 \_ PASSPORT \_ 驗證 | Microsoft Passport 驗證已停用。 此為預設值。 |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ 停用 \_ PASSPORT \_ KEYRING | Passport keyring 已停用。 此為預設值。 |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ 啟用 \_ PASSPORT \_ 驗證 | Passport 驗證已啟用。 |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ 啟用 \_ PASSPORT \_ KEYRING | Passport keyring 已啟用。 |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP \_ 選項 \_ 連接 \_ 重試**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含連接到主機的 timesWinHTTP 嘗試次數。 Microsoft Windows HTTP Services (WinHTTP) 每個網際網路通訊協定只會嘗試一次 (IP) 位址。 例如，如果您嘗試連線到有10個 IP 位址的多重主目錄主機，而 **winHTTP \_ 選項連線 \_ \_ 重試** 設定為7，則 winHTTP 只會嘗試連線到前七個 ip 位址。 假設有一組相同的10個 IP 位址，則當 **winHTTP \_ 選項 \_ 連接 \_ 重試** 設定為20時，winHTTP 只會嘗試10次。 如果連接嘗試在指定的嘗試次數之後仍失敗，或連接逾時之前已過期，則會取消要求。 **WINHTTP \_ 選項 \_ 連接 \_ 重試** 的預設值為五次嘗試。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ 選項 \_ 連接 \_ 超時**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含超時時間值（以毫秒為單位）。 將此選項設定為無限 (0xFFFFFFFF) 將會停用此計時器。

如果 TCP 連線要求所花費的時間超過這個超時值，就會取消要求。 預設的超時時間為60秒。 當您嘗試連線到單一主機 (多個 IP 位址時，) 的多重主控制項，則會有每個個別連接的時間限制。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP \_ 選項 \_ 連接 \_ 資訊**
</dt> <dd> <dl> <dt>



抓取 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回時產生回應之要求的來源和目的地 IP 位址和埠。 應用程式會使用 **WINHTTP \_ 選項 \_ 連接 \_ 資訊** 選項來呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ，並在 *lpBuffer* 參數中提供 [**winHTTP \_ 連接 \_ 資訊**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)結構。 如需詳細資訊，請參閱 **WINHTTP \_ 連接 \_ 資訊**。

**Windows Server 2003 （含 SP1）和 Windows XP SP2：** 此旗標已淘汰。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V0**
</dt> <dd> <dl> <dt>



針對要求所使用的基礎連接，擷取 [**TCP \_ 資訊 \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) 結構。 傳回的結構可能包含透過相同連接傳送的先前要求的統計資料。

> [!Note]
> **WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1** 已取代此選項。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1**
</dt> <dd> <dl> <dt>



擷取要求所使用之基礎連接的 [**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) 結構。 傳回的結構可能包含透過相同連接傳送的先前要求的統計資料。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP \_ 選項 \_ 內容 \_ 值**
</dt> <dd> <dl> <dt>



設定或抓取 DWORD 指標，其中包含與這個 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼相關聯之內容值的指標。 **\_** 使用儲存在緩衝區中的值，並為 **WINHTTP \_ 選項 \_ 內容 \_ 值** 選項旗標指派新值。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP \_ 選項 \_ 解壓縮**
</dt> <dd> <dl> <dt>



設定旗標的 DWORD，以判斷 WinHTTP 是否會自動以壓縮的內容編碼方式解壓縮回應主體。 WinHTTP 也會設定適當的 Accept-Encoding 標頭，覆寫呼叫端所提供的任何一個。 支援的值為：

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ GZIP | 解壓縮內容編碼： gzip 回應。 |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ DEFLATE | 解壓縮內容編碼： deflate 回應。 |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ 全部 | 使用任何支援的內容編碼來將回應解壓縮。 |

根據預設，WinHTTP 會將壓縮的回應傳遞給未修改的呼叫端。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP \_ 選項 \_ 停用 \_ CERT \_ 鏈 \_ 建立**
</dt> <dd> <dl> <dt>


在 WinHttp 會話控制碼上設定這個選項，可讓您啟用/停用伺服器憑證鏈是否已建立。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP \_ 選項 \_ 停用 \_ 功能**
</dt> <dd> <dl> <dt>



設定不帶正負號的長整數值，指定使用下列其中一個或多個旗標停用的功能。 請注意，只有在使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立要求控制碼之後，以及使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)傳送要求之前，才應將這項功能傳遞至要求控制碼上的 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ 停用 \_ 驗證 | 自動驗證已停用。 |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ 停用 \_ COOKIE | 已停用自動將 cookie 標頭新增至要求的功能。 此外，傳回的 cookie 也不會自動新增至 cookie 資料庫。 停用 cookie 可能會導致 Passport 驗證效能不佳。 |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ 停用 \_ 保持運作 \_ 狀態 | 停用連接的 keep-alive 語義。 MSN、NTLM 和其他類型的驗證都需要 keep-alive 語義。 |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP \_ 停用重新 \_ 導向 | 使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)傳送要求時，自動重新導向已停用。 如果自動重新導向已停用，應用程式必須註冊回呼函式，Passport 驗證才會成功。 |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP \_ 選項 \_ 停用 \_ 安全 \_ 通訊協定 \_ 回復**
</dt> <dd> <dl> <dt>



當初始通訊協定協商失敗時，防止 WinHTTP 使用較低版本的安全性通訊協定來重試連接。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP \_ 選項 \_ 停用 \_ 串流 \_ 佇列**
</dt> <dd> <dl> <dt>



允許新的要求在達到最大並行串流限制時開啟額外的 HTTP/2 連接，而不是在現有的連接上等候下一個可用的資料流程。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP \_ 選項 \_ 啟用 \_ 功能**
</dt> <dd> <dl> <dt>



設定不帶正負號的長整數值，指定目前已啟用的功能。 可以是下列其中一個值。

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ 啟用 \_ SSL \_ 還原 \_ 模擬 | 如果啟用，WinHTTP 會暫時還原 SSL 憑證驗證作業期間的用戶端模擬。 此值只能在會話控制碼上進行設定。 |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ 啟用 \_ SSL \_ 撤銷 | 啟用時，WinHTTP 允許 SSL 撤銷。 此值只能在要求控制碼上進行設定。 |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP \_ 選項 \_ 啟用 \_ HTTP \_ 通訊協定**
</dt> <dd> <dl> <dt>



設定可接受之 advanced HTTP 版本的 DWORD 位元遮罩。 可能的值包括：

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP \_ 通訊協定 \_ 旗標 \_ HTTP2 (0x1)  | 針對要求啟用 HTTP/2。 |
| 無 (0x0)  | 將要求限制為 HTTP/1.1 及更早的版本。 |

舊版的 HTTP (1.1 和先前的) 無法使用這個選項停用。 預設值為0x0。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP \_ 選項 \_ ENABLE \_ HTTP2 \_ PLUS \_ CLIENT \_ CERT**
</dt> <dd> <dl> <dt>


您可以在 WinHttp 會話控制碼上設定這個選項，讓 WinHttp 在使用 HTTP/2 時，使用呼叫端提供的用戶端憑證內容。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP \_ 選項 \_ ENABLETRACING**
</dt> <dd> <dl> <dt>



設定 **布林** 值，這個值會指定目前是否已啟用追蹤。 如需 WinHTTP 中追蹤設備的詳細資訊，請參閱 [WinHTTP 追蹤設備](winhttptracecfg-exe--a-trace-configuration-tool.md)。 此選項只能在 **Null** **HINTERNET** 控制碼上進行設定。


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ 選項 \_ 編碼 \_ 額外**
</dt> <dd> <dl> <dt>



啟用路徑和查詢字串的 URL 百分比編碼。

或者，您可以在呼叫 WinHttp 之前對編碼百分比進行編碼。

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP \_ 選項 \_ 到期 \_ 連接**
</dt> <dd> <dl> <dt>



此選項只能在要求控制碼上設定，而該控制碼仍在使用中 (傳送或接收) 。 設定此選項會告知 WinHttp 在與傳入的要求控制碼相關聯的連接上停止服務要求。 當要求控制碼完成時，將會關閉此連接。 此選項不會使用任何參數。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP \_ 選項 \_ 延伸 \_ 錯誤**
</dt> <dd> <dl> <dt>



抓取不帶正負號的長整數值，其中包含與 \_ \_ \* 此執行緒內容中最後傳回的錯誤 WINHTTP 錯誤訊息對應的 Microsoft Windows 通訊端錯誤碼。 您可以傳遞 **Null** 做為控制碼值。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP \_ 選項 \_ FIRST \_ 可用 \_ 連接**
</dt> <dd> <dl> <dt>


根據預設，當 WinHttp 傳送要求時，如果沒有可用的連線來處理要求，WinHttp 將會嘗試建立新的連線，並將要求系結至這個新連接。 當您設定此選項時，會改為在第一個可用的連接上提供這類要求，而不一定是要建立的連接。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP \_ 選項 \_ 全域 \_ PROXY \_ 認證**
</dt> <dd> <dl> <dt>



將 *hInternet* 函式參數設定為 **Null** 的 [**WINHTTP 認證 \_ \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)結構的指標。 此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet 設定！ShareCredsWithWinHttp**。 如果未設定此登錄機碼，WinHTTP 將會傳回錯誤： **\_ winHTTP \_ 無效 \_ 選項** 的錯誤。 依預設，此登錄機碼不存在。 當設定時，WinINet 會將認證傳送至 WinHTTP。 每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。 為了共用 proxy 認證以外的伺服器認證，使用者必須設定 **WINHTTP \_ 選項 [ \_ 使用 \_ 全域 \_ 伺服器 \_ 認證** ]。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP \_ 選項 \_ 全域 \_ 伺服器 \_ 認證**
</dt> <dd> <dl> <dt>



將 *hInternet* 函式參數設定為 **Null** 的 [**WINHTTP 認證 \_ \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)結構的指標。 此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet 設定！ShareCredsWithWinHttp**。 如果未設定此登錄機碼，WinHTTP 將會傳回錯誤： **\_ winHTTP \_ 無效 \_ 選項** 的錯誤。 依預設，此登錄機碼不存在。 當設定時，WinINet 會將認證傳送至 WinHTTP。 每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。 為了共用 proxy 認證以外的伺服器認證，使用者必須設定 **WINHTTP \_ 選項 [ \_ 使用 \_ 全域 \_ 伺服器 \_ 認證** ]。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP \_ 選項 \_ 控制碼 \_ 類型**
</dt> <dd> <dl> <dt>



抓取不帶正負號的長整數值，其中包含傳入的 [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼類型。 傳回值可以是下列其中一個：

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 連接 | 控制碼是連接控制碼。 |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 要求 | 控制碼是要求控制碼。 |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 會話 | 控制碼是會話控制碼。 |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_需要 WINHTTP 選項 \_ HTTP \_ 通訊協定 \_**
</dt> <dd> <dl> <dt>



防止 **WINHTTP \_ 選項啟用 \_ \_ HTTP \_ 通訊協定** 以外的通訊協定版本使用於要求。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**使用的 WINHTTP \_ 選項 \_ HTTP \_ 通訊協定 \_**
</dt> <dd> <dl> <dt>



取得 DWORD，指出指定的要求上使用的是哪個先進的 HTTP 版本。 如需可能值的清單，請參閱 **WINHTTP \_ 選項 \_ ENABLE \_ HTTP \_ PROTOCOL**。



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP \_ 選項 \_ HTTP \_ 版本**
</dt> <dd> <dl> <dt>



設定或抓取 [**HTTP \_ 版本 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) 結構，其中包含所支援的 HTTP 版本。 這是整個進程的選項;針對控制碼使用 **Null** 。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP \_ 選項 \_ HTTP2 \_ KEEPALIVE**
</dt> <dd> <dl> <dt>


您可以在會話控制碼上設定這個選項，讓 WinHttp 使用 HTTP/2 偵測框架作為 keepalive 機制。 呼叫端指定的超時時間（以毫秒為單位），且在該超時期間的連線上沒有任何活動之後，WinHttp 將開始傳送 HTTP/2 偵測畫面。 呼叫端無法設定小於5000毫秒的超時值。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP \_ 選項 \_ HTTP2 \_ PLUS \_ 傳輸 \_ 編碼**
</dt> <dd> <dl> <dt>


您可以在 WinHttp 要求控制碼上設定這個選項，以控制當 HTTP/2 回應包含「傳輸編碼」標頭時，WinHttp 的行為方式。 在這種情況下，如果此選項設定為 **FALSE**，WinHttp 將會傳回錯誤。


</dt> </dl> </dd> <dt>


<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP \_ 選項會 \_ 離線略過憑證 \_ \_ 撤銷 \_**
</dt> <dd> <dl> <dt>



允許安全連線使用無法下載憑證撤銷清單的安全性憑證。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP \_ 選項 \_ IPV6 \_ FAST \_ FALLBACK**
</dt> <dd> <dl> <dt>



啟用 IPv6 快速回復 (更滿意的連接 Eyeballs) 。 這種行為與 [RFC 6555](https://tools.ietf.org/html/rfc6555) 中所述的快樂 Eyeballs 行為類似，可在 IPv6 不可靠的網路上改善連線時間。
- 如果為指定的主機解析 IPv6 和 IPv4 位址，WinHttp 將會先以短暫的 (300 毫秒) timeout 來連線至第一個已解析的 IPv6 位址。
- 如果連線失敗，WinHttp 將嘗試以標準超時連接到第一個已解析的 IPv4 位址。
- 第二個連接失敗時，WinHttp 會以標準超時重試第一個已解析的 IPv6 位址。
- 第三個連接失敗時，WinHttp 會還原為任何剩餘位址的預設行為，並嘗試使用標準超時連接到每一個位址，直到建立連線或未保留任何位址為止。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP \_ 選項 \_ 為 \_ PROXY \_ CONNECT \_ 回應**
</dt> <dd> <dl> <dt>



取得是否可以取得 Proxy 傳回連線回應。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_ \_ \_ \_ 每 \_ 1 \_ 0 部 \_ 伺服器的 WINHTTP 選項 MAX CONNS**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含每個 HTTP/1.0 伺服器允許的最大連接數目。 預設值為 [ **無限**]。

**Windows Vista SP1 和 Windows Server 2008：** 此旗標已淘汰。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**每一伺服器的 WINHTTP \_ 選項 \_ MAX \_ CONNS \_ \_**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含每個伺服器允許的最大連接數目。 預設值為 [ **無限**]。

當此選項設定為零時，WinHTTP 會將連接數目的限制設定為2。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 自動重新 \_ 導向**
</dt> <dd> <dl> <dt>



設定 WinHTTP 遵循的重新導向數目上限;預設值為10。 這項限制可防止未經授權的網站使 WinHTTP 用戶端在大量重新導向之後暫停。

**Windows XP SP1 和 Windows 2000 SP3：** 此旗標已淘汰。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 狀態 \_ 繼續**
</dt> <dd> <dl> <dt>



將最終狀態代碼傳回至 WinHTTP 用戶端之前，已忽略參考最大的資訊100-199 狀態碼回應數目。 資訊100-199 狀態碼可由伺服器在最終狀態代碼之前傳送，如需詳細資訊，請參閱 HTTP/1.1 的規格 (如需詳細資訊，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)) 。 預設值為 10。

**Windows XP SP1 和 Windows 2000 SP3：** 此旗標已淘汰。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ 選項 \_ \_ 回應 \_ 清空最 \_ 大值**
</dt> <dd> <dl> <dt>



系結至從回應中清空的資料量，以重複使用連接（以位元組指定）。 預設值為1MB。

**Windows XP SP1 和 Windows 2000 SP3：** 此旗標已淘汰。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP \_ 選項 \_ 的 \_ 回應 \_ 標頭 \_ 大小上限**
</dt> <dd> <dl> <dt>



伺服器回應的標頭部分大小上限的系結集，以位元組為單位來指定。 這項系結會透過傳送無限標頭資料的回應，來保護用戶端免于嘗試停止用戶端的未經授權伺服器。 預設值是64KB。

**Windows XP SP1 和 Windows 2000 SP3：** 此旗標已淘汰。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP \_ 選項 \_ 父 \_ 控制碼**
</dt> <dd> <dl> <dt>



捕獲此控制碼的父控制碼。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ 文字**
</dt> <dd> <dl> <dt>



抓取包含 Passport 登入伺服器所提供之 [*cobranding*](glossary.md) 文字的字串。 當登入伺服器以401狀態碼回應時，應立即取出此選項。 應用程式應該以位元組為單位，以位元組為單位，且足以容納傳回的字串。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ URL**
</dt> <dd> <dl> <dt>



抓取包含 Passport 登入伺服器所提供之 [*cobranding*](glossary.md) 圖形 URL 的字串。 當登入伺服器以401狀態碼回應時，應立即取出此選項。 應用程式應該以位元組為單位，以位元組為單位，且足以容納傳回的字串。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ RETURN \_ URL**
</dt> <dd> <dl> <dt>



在要求控制碼上設定唯讀選項，以抓取 Passport 傳回 URL。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ 登出 \_**
</dt> <dd> <dl> <dt>



將會話控制碼上的選項設定為登出任何 Passport 登入。 應用程式應該傳入 Passport 傳回 URL，此 URL 是以 **WINHTTP \_ 選項 \_ Passport \_ return \_ url** 抓取。 系統會清除所有與傳回 URL 相關的 cookie。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP \_ 選項 \_ 密碼**
</dt> <dd> <dl> <dt>



設定或抓取包含與要求控制碼相關聯之密碼的字串值。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP \_ 選項 \_ PROXY**
</dt> <dd> <dl> <dt>



設定或抓取 [**WINHTTP \_ PROXY \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) 結構，其中包含現有會話控制碼或要求控制碼上的 PROXY 資料。 在抓取 proxy 資料時，應用程式必須釋放此結構中所包含的 **lpszProxy** 和 **lpszProxyBypass** 字串 (如果它們是非 **Null**) 使用 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函數。 應用程式可以藉由傳遞 **Null** 控制碼 (預設 proxy) 來查詢全域 proxy 資料。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP \_ 選項 \_ PROXY \_ 密碼**
</dt> <dd> <dl> <dt>



設定或抓取包含用來存取 proxy 之密碼的字串值。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**已 \_ 使用 WINHTTP 選項 \_ PROXY \_ SPN \_**
</dt> <dd> <dl> <dt>



取得 WinHTTP 在驗證期間提供給 SSPI 的 proxy 伺服器主體名稱。 這個字串值會在驗證失敗後 usefor 傳遞至 [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) 。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP \_ 選項 \_ PROXY 使用者 \_ 名稱**
</dt> <dd> <dl> <dt>



設定或抓取包含用來存取 proxy 之使用者名稱的字串值。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP \_ 選項 \_ 讀取 \_ 緩衝區 \_ 大小**
</dt> <dd> <dl> <dt>



此選項已被取代;它沒有任何作用。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP \_ 選項 \_ 接收 \_ PROXY \_ CONNECT \_ 回應**
</dt> <dd> <dl> <dt>



設定是否可以取出 proxy 回應實體。 預設會停用這個選項。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含要等候接收要求的所有回應標頭的超時值（以毫秒為單位）。 如果 WinHTTP 無法在此超時期間內接收所有標頭，則會取消要求。 預設的超時值為90秒。

只有從通訊端接收資料時，才會檢查此超時時間。 如此一來，當超時時間過期時，用戶端應用程式就不會收到通知，直到伺服器的資料抵達為止。 如果沒有資料從伺服器抵達，用戶端應用程式的超時期限和通知之間的延遲可能會與使用 [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)函數的 *dwReceiveTimeout* 參數所設定的超時值相同。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP \_ 選項 \_ 接收 \_ 超時**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含接收要求的部分回應或讀取某些資料的超時時間值（以毫秒為單位）。 如果回應時間超過這個超時值，就會取消要求。 預設的逾時值是 30 秒。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP \_ 選項重新 \_ 導向 \_ 原則**
</dt> <dd> <dl> <dt>



設定 WinHTTP 的行為，關於處理一倍的 HTTP 重新導向狀態碼。 您可以在會話或要求控制碼上將此選項設定為下列其中一個值：

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP \_ 選項的重新 \_ 導向 \_ 原則 \_ 一律 | 所有重新導向都會自動遵循。 |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP \_ 選項重新 \_ 導向 \_ 原則不 \_ 允許 \_ HTTPS \_ 至 \_ HTTP | 除了源自安全 (HTTPs) URL 到不安全的 (HTTP) URL 以外的所有重新導向。 這是預設值。 |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP \_ 選項重新 \_ 導向 \_ 原則 \_ 永不 | 重新導向永遠不會跟著進行。 這會將30倍的狀態傳回給應用程式。 |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP \_ 選項 \_ 拒絕 \_ \_ URL 中的 USERPWD \_**
</dt> <dd> <dl> <dt>



拒絕包含使用者名稱和密碼的 Url。 即使未指定使用者名稱或密碼，此選項也會拒絕包含 *username： password* 語義的 url。 例如，" u:p@hostname "、" :@hostname "、" u:@hostname " 和 " :p@hostname " 都會標示為無效。 如果將不正確 URL 傳遞至函式，則會傳回 [錯誤 \_ WINHTTP 不正確 \_ \_ url](error-messages.md)。 根據預設，這個選項是關閉的。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP \_ 選項 \_ 要求 \_ 優先順序**
</dt> <dd> <dl> <dt>



此選項已被取代;它沒有任何作用。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP \_ 選項 \_ 要求 \_ 統計資料**
</dt> <dd> <dl> <dt>



擷取要求的統計資料。  如需可用的統計資料清單，請參閱 [**WINHTTP \_ 要求 \_ 統計**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)資料。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP \_ 選項 \_ 要求 \_ 時間**
</dt> <dd> <dl> <dt>



擷取要求的計時資訊。 如需可用的時間清單，請參閱 [**WINHTTP \_ 要求 \_ 時間**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP \_ 選項 \_ 需要 \_ STREAM \_ END**
</dt> <dd> <dl> <dt>


此選項會告知 WinHttp 略過「內容長度」回應標頭，並繼續接收串流，直到收到 END_STREAM 旗標為止。



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP \_ 選項 \_ 解析 \_ 主機名稱**
</dt> <dd> <dl> <dt>


您可以在 WinHttp 要求控制碼上設定這個選項，然後再傳送。 如果設定，WinHttp 將使用呼叫端提供的字串作為 DNS 解析的主機名稱。



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP \_ 選項 \_ 解析 \_ 超時**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含用來解析主機名稱的超時時間值（以毫秒為單位）。 預設的超時值是 **無限** 的。 如果指定了非預設值，每個名稱解析都有一個執行緒建立的額外負荷。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP \_ 選項 \_ 安全 \_ 通訊協定**
</dt> <dd> <dl> <dt>



設定不帶正負號的長整數值，指定可接受哪些安全通訊協定。 依預設，只有 SSL3 和 TLS1 會在 Windows 7 和 Windows 8 中啟用。 依預設，只有 SSL3、tls 1.0、tls 1.1 和 tls 1.2 會在 Windows 8.1 和 Windows 10 中啟用。 值可以是下列一或多個值的組合。

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ 全部 | 您可以使用安全通訊端層 (SSL) 2.0、SSL 3.0 和傳輸層安全性 (TLS) 1.0 通訊協定。 |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ SSL2 | 您可以使用 SSL 2.0 通訊協定。 |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ SSL3 | 您可以使用 SSL 3.0 通訊協定。 |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1 | 您可以使用 TLS 1.0 通訊協定。 |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1 \_ 1 | 您可以使用 TLS 1.1 通訊協定。 |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1 \_ 2 | 您可以使用 TLS 1.2 通訊協定。 |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 憑證 \_ 結構**
</dt> <dd> <dl> <dt>



抓取 SSL/TLS 伺服器到 [**WINHTTP \_ 憑證 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) 結構中的憑證。 應用程式必須使用 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)釋放 **lpszSubjectInfo** 和 **lpszIssuerInfo** 成員。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 旗標**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含控制碼的安全性旗標。 它可以是下列值的組合：

| 詞彙 | 描述 |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>安全性 \_ 旗標 \_ 忽略 \_ CERT \_ CN \_ 無效 |允許在憑證中使用不正確一般名稱;亦即，應用程式所指定的伺服器名稱不符合憑證中的一般名稱。 如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標 \_ CERT \_ CN \_ 無效** 的回呼。 |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>安全性 \_ 旗標 \_ 忽略憑證 \_ \_ 日期 \_ 無效 |允許不正確憑證日期，也就是過期或尚未有效的憑證。 如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標憑證 \_ \_ 日期 \_ 無效** 的回呼。 |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>安全性 \_ 旗標 \_ 忽略 \_ 未知的 \_ CA | 允許不正確憑證授權單位單位。 如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標 \_ 不正確 \_ CA** 回呼。 |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>安全性 \_ 旗標 \_ 忽略憑證錯誤的 \_ \_ \_ 使用方式 | 允許以非伺服器憑證建立伺服器的身分識別 (例如，) 的用戶端憑證。 |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>安全性 \_ 旗標 \_ 忽略 \_ 弱 \_ 式簽章 | 允許忽略弱式簽章。<br/>從 Windows 7 和 Windows Server 2008 R2 開始，每個 OS 的匯總套件更新中都可以使用此旗標。 |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>安全性 \_ 旗標 \_ 安全 | 使用安全傳輸。 這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。 |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>安全性 \_ 旗標 \_ 強度 \_ 中 | 使用中型 (56 位) 加密。 這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。 |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>安全性 \_ 旗標 \_ 強度 \_ 強 | 使用強式 (128 位) 加密。 這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。 |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>安全性 \_ 旗標 \_ 強度 \_ 弱 | 使用弱式 (40 位) 加密。 這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。 |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 資訊**
</dt> <dd> <dl> <dt>



擷取要求的 SChannel 連線和加密資訊。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 金鑰 \_ 位**
</dt> <dd> <dl> <dt>



抓取不帶正負號的長整數值，其中包含加密金鑰的加密強度。 較大的數位表示較強的加密強度加密。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP \_ 選項 \_ 傳送 \_ 超時**
</dt> <dd> <dl> <dt>



設定或抓取不帶正負號的長整數值，其中包含要傳送要求或寫入部分資料的超時時間值（以毫秒為單位）。 如果傳送要求的時間超過超時時間，則會取消傳送作業。 預設的超時時間為30秒。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ CBT**
</dt> <dd> <dl> <dt>



取得 SecPkgCoNtext 系結 [**結構 \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) 的指標，此結構會指定 (CBT) 的通道系結 Token。

通道系結權杖是安全傳輸通道的屬性，可用來將驗證通道系結至安全傳輸通道。 只有在建立 SSL 連線之後，此選項才能取得此權杖。

> [!Note]
> 傳遞此選項和 *lpBuffer* 至 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)的 **null** 值，將會傳回 \_ 錯誤 \_ 的緩衝區，以及 *lpdwBufferLength* 參數中緩衝區的必要位元組大小。 這個傳回的緩衝區大小值可以在後續的呼叫中傳遞，以查詢通道系結 Token。 \_ \_ \_ 如果您想要根據通道系結 Token 修改要求標頭，則在處理 WINHTTP 回呼狀態要求時，必須執行這些步驟。 請注意，Windows XP 和 Vista 不支援在此回呼期間修改要求標頭。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 鏈 \_ 內容**
</dt> <dd> <dl> <dt>



抓取伺服器憑證鏈內容。 **WINHTTP \_可以傳遞選項 \_ 伺服器憑證 \_ \_ 鏈 \_ 內容** ，以取得在協商 SSL 連線期間收到的伺服器憑證鏈的憑證 **\_ 鏈 \_ 內容** 重複指標。 用戶端必須在[](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)填入緩衝區的傳回 PCCERT \_ 內容指標上呼叫 CertFreeCertificateCoNtext。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 內容**
</dt> <dd> <dl> <dt>



抓取伺服器認證內容。 **WINHTTP \_您可以傳遞選項 \_ 伺服器憑證 \_ \_ 內容** ，以取得在協商 SSL 連線期間收到之伺服器憑證的憑證 [**內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) 重複指標。 用戶端必須在[](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)填入緩衝區的傳回 PCCERT \_ 內容指標上呼叫 CertFreeCertificateCoNtext。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**已 \_ 使用 WINHTTP 選項 \_ 伺服器 \_ SPN \_**
</dt> <dd> <dl> <dt>



取得 WinHTTP 在驗證期間提供給 SSPI 的伺服器伺服器主體名稱。 在驗證失敗之後，這個字串值可以傳遞給 [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) 。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP \_ 選項 \_ SPN**
</dt> <dd> <dl> <dt>



在建立 Kerberos 或協商 Kerberos 驗證的 SPN (服務主體名稱) 時，包含或移除伺服器埠號碼。 此旗標是下列其中一個值：

| 詞彙 | 描述 |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ 停用 \_ SPN \_ 伺服器 \_ 埠 | 移除伺服器埠號碼。 |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ 啟用 \_ SPN \_ 伺服器 \_ 埠 | 包括伺服器埠號碼。 |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP \_ 選項 \_ 資料流程 \_ 錯誤碼 \_**
</dt> <dd> <dl> <dt>


此選項可在 WinHttp 要求控制碼上進行查詢，並會傳回由 HTTP 資料流程接收的 RST_STREAM 框架所指出的錯誤碼。



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP \_ 選項 \_ TCP \_ FAST \_ 開啟**
</dt> <dd> <dl> <dt>



啟用連接的 TCP Fast Open。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP \_ 選項 \_ TCP \_ KEEPALIVE**
</dt> <dd> <dl> <dt>



您可以在 WinHttp 會話控制碼上設定這個選項，以啟用基礎通訊端上的 TCP 保持連線行為。 接受 [**tcp \_ keepalive**](/windows/win32/winsock/sio-keepalive-vals) 結構。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP \_ 選項 \_ TLS \_ FALSE \_ START**
</dt> <dd> <dl> <dt>



啟用連接的 TLS False Start。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP \_ 選項 \_ TLS \_ 通訊協定不 \_ 安全 \_ 的回復**
</dt> <dd> <dl> <dt>



您可以在 WinHttp 會話控制碼上設定這個選項，以控制如果有較新的通訊協定版本的 TLS 交握失敗，是否允許回溯至 TLS 1.0。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP \_ 選項 \_ UNLOAD \_ 通知 \_ 事件**
</dt> <dd> <dl> <dt>



取得將在特定會話的最後一個回呼完成時設定的事件。 此旗標必須用於會話控制碼。 事件必須等到 WinHTTP 設定後才能關閉。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ 選項 \_ UNSAFE \_ 標頭 \_ 剖析**
</dt> <dd> <dl> <dt>



此選項已保留供內部使用，不應該呼叫。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP \_ 選項 \_ 升級 \_ 至 \_ WEB \_ 通訊端**
</dt> <dd> <dl> <dt>



指示堆疊使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)啟動 WebSocket 交握處理常式。 此選項不會使用任何參數。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP \_ 選項 \_ URL**
</dt> <dd> <dl> <dt>



抓取字串值，其中包含已下載資源的完整 URL。 如果原始 URL 包含任何額外的資料（例如搜尋字串或錨點），或重新導向呼叫，則傳回的 URL 會與原始的 URL 不同。 應用程式應該傳入緩衝區（以位元組為單位），這夠大，足以將傳回的 URL 保存在寬字元中。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP \_ 選項 \_ 使用 \_ 全域 \_ 伺服器 \_ 認證**
</dt> <dd> <dl> <dt>



採用 **BOOL** ，而且只能設定會話控制碼。 它只會在設定選項之後，向下傳播至從會話控制碼建立的控制碼。 若 **為 TRUE**，則此選項會導致最後使用從 WinInet 推入的全域伺服器認證。 此選項的預設值為 **FALSE**。 此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet 設定！ShareCredsWithWinHttp**。 依預設，此登錄機碼不存在。 當設定時，WinINet 會將認證傳送至 WinHTTP。 每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP \_ 選項 \_ 使用者 \_ 代理程式**
</dt> <dd> <dl> <dt>



設定或抓取 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)提供的控制碼上的 [*使用者代理程式*](glossary.md)字串，並在後續的 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式中使用，但前提是它不是由 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)或 **WinHttpSendRequest** 所加入的標頭所覆寫。 在抓取使用者代理程式時，應用程式應該傳入緩衝區（以位元組為單位），這夠大，足以將傳回的 URL 保存在寬字元中。 設定使用者代理程式時，緩衝區大小是字串的長度（以字元為單位），加上 **Null** 結束字元。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP \_ 選項使用者 \_ 名稱**
</dt> <dd> <dl> <dt>



設定或抓取包含使用者名稱的字串。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 關閉 \_ 超時**
</dt> <dd> <dl> <dt>



設定 [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) 應該等候才能完成關閉信號交換的時間（以毫秒為單位）。 預設值是 10 秒。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔**
</dt> <dd> <dl> <dt>



設定透過連接傳送 keep-alive 封包的間隔（以毫秒為單位）。 預設間隔為 30000 (30 秒) 。 最小間隔為 15000 (15 秒) 。 使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 設定低於15000的值，將會傳回 **錯誤 \_ 不正確 \_ 參數**。

> [!Note]
> **WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔** 的預設值是從 **HKLM： \\ SOFTWARE \\ Microsoft \\ WebSocket \\ KeepaliveInterval** 進行讀取。 如果未設定值，則會使用預設值30000。 的 keepalive 間隔不能低於15000毫秒。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 接收 \_ 緩衝區 \_ 大小**
</dt> <dd> <dl> <dt>



設定或抓取 DWORD，以指定要用於 WebSocket 連接的接收緩衝區大小。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 傳送 \_ 緩衝區 \_ 大小**
</dt> <dd> <dl> <dt>



設定或抓取 DWORD，以指定要用於 WebSocket 連接的傳送緩衝區大小。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP \_ 選項背景 \_ 工作 \_ 執行緒 \_ 計數**
</dt> <dd> <dl> <dt>



設定不帶正負號的長整數值，指定執行緒集區應用於非同步完成的背景工作執行緒數目。 此選項的預設值為零，表示工作者執行緒的數目等於系統上的 Cpu 數目。 此選項只能在發生非同步作業之前，在 **Null**  [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼上設定。 此選項只能設定一次。

**Windows Server 2008 R2 和 Windows 7：** 此旗標已淘汰。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP \_ 選項 \_ 寫入 \_ 緩衝區 \_ 大小**
</dt> <dd> <dl> <dt>



此選項已被取代;它沒有任何作用。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

下表列出選項旗標，方法是指定它們可以處理的控制碼、是否可以查詢和設定，以及使用的資料類型。 「X」表示選項旗標適用于與函式或控制碼搭配使用，而「-」指定選項旗標無效。

如果您嘗試在不支援的 Windows 版本上設定或查詢選項旗標，將會導致 **錯誤 \_ WINHTTP \_ 不正確 \_ 選項**。

| 選項旗標和資料類型 | 會話控制碼 | 要求控制碼 | 查詢選項 | Set 選項 | 最小 Windows 版本 |
|-|-|-|-|-|-|
| WINHTTP \_ 選項有 \_ 保證 \_ 非 \_ 封鎖 \_ 回呼<br/>**BOOL** | X | \- | \- | X | \- |
| WINHTTP \_ 選項 \_ 自動登入 \_ 原則<br/>**DWORD** | \- | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 背景 \_ 連接<br/>**DWORD** | X | \- | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ 回呼<br/>**LPVOID** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容<br/>[**憑證 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單<br/>[**SecPkgCoNtext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| WINHTTP \_ 選項 \_ 字碼頁<br/>**DWORD** | X | \- | \- | X | \- |
| WINHTTP \_ 選項 \_ 設定 \_ PASSPORT \_ 驗證<br/>**DWORD** | X | \- | \- | X | \- |
| WINHTTP \_ 選項 \_ 連接 \_ 重試<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 連接 \_ 超時<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 連接 \_ 資訊<br/>[**WINHTTP \_ 連接 \_ 資訊**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V0<br/>[**TCP \_ 資訊 \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10版本1903 |
| WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1<br/>[**TCP \_ 資訊 \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10版本2004 |
| WINHTTP \_ 選項 \_ 內容 \_ 值<br/>**DWORD \_ PTR** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 解壓縮<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| WINHTTP \_ 選項 \_ 停用 \_ CERT \_ 鏈 \_ 建立<br/>**BOOL** | X | \- | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ 停用 \_ 功能<br/>**DWORD** | \- | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 停用 \_ 安全 \_ 通訊協定 \_ 回復<br/>**BOOL** | X | \- | \- | X | Windows 10版本1903 |
| WINHTTP \_ 選項 \_ 停用 \_ 串流 \_ 佇列<br/>**BOOL** | X | X | \- | X | Windows 10版本1809 |
| WINHTTP \_ 選項 \_ 啟用 \_ 功能<br/>**DWORD** | \* | \* | \- | X | \- |
| WINHTTP \_ 選項 \_ 啟用 \_ HTTP \_ 通訊協定<br/>**DWORD** | X | X | \- | X | Windows 10 版本 1607 |
| WINHTTP \_ 選項 \_ ENABLE \_ HTTP2 \_ PLUS \_ CLIENT \_ CERT \_ CONTEXT<br/>**BOOL** | X | \- | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ ENABLETRACING<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP \_ 選項 \_ 編碼 \_ 額外<br/>**BOOL** | X | X | \- | X | Windows 10版本1803 |
| WINHTTP \_ 選項 \_ 到期 \_ 連接<br/>N/A | \- | X | \- | X | Windows 10版本1903 |
| WINHTTP \_ 選項 \_ 延伸 \_ 錯誤<br/>**DWORD** | X | X | X | \- | \- |
| WINHTTP \_ 選項 \_ FIRST \_ 可用 \_ 連接<br/>**BOOL** | X | \- | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ 全域 \_ PROXY \_ 認證<br/>[**WINHTTP \_ 認證**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 全域 \_ 伺服器 \_ 認證<br/>[**WINHTTP \_ 認證 \_ 例如**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 控制碼 \_ 類型<br/>**DWORD** | X | X | X | \- | \- |
| \_需要 WINHTTP 選項 \_ HTTP \_ 通訊協定 \_<br/>**BOOL** | X | X | \- | X | Windows 10版本1903 |
| 使用的 WINHTTP \_ 選項 \_ HTTP \_ 通訊協定 \_<br/>**DWORD** | \- | X | X | \- | Windows 10 版本 1607 |
| WINHTTP \_ 選項 \_ HTTP \_ 版本<br/>[**HTTP \_ 版本 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ HTTP2 \_ KEEPALIVE<br/>**DWORD** | X | \- | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ HTTP2 \_ PLUS \_ 傳輸 \_ 編碼<br/>**BOOL** | X | X | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項會 \_ 離線略過憑證 \_ \_ 撤銷 \_<br/>**BOOL** | \- | X | \- | X | Windows 10版本2004 |
| WINHTTP \_ 選項 \_ IPV6 \_ FAST \_ FALLBACK<br/>**BOOL** | X | \- | \- | X | Windows 10版本1903 |
| WINHTTP \_ 選項 \_ 為 \_ PROXY \_ CONNECT \_ 回應<br/>**BOOL** | X | X | X | \- | \- |
| \_ \_ \_ \_ 每 \_ 1 \_ 0 部 \_ 伺服器的 WINHTTP 選項 MAX CONNS<br/>**DWORD** | X | \- | X | X | \- |
| 每一伺服器的 WINHTTP \_ 選項 \_ MAX \_ CONNS \_ \_<br/>**DWORD** | X | \- | X | X | \- |
| WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 自動重新 \_ 導向<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 狀態 \_ 繼續<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ \_ 回應 \_ 清空最 \_ 大值<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 的 \_ 回應 \_ 標頭 \_ 大小上限<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 父 \_ 控制碼<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ 文字<br/>**LPWSTR** | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ URL<br/>**LPWSTR** | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ PASSPORT \_ RETURN \_ URL<br/>**LPVOID** | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ PASSPORT \_ 登出 \_<br/>**LPVOID** | X | \- | \- | X | \- |
| WINHTTP \_ 選項 \_ 密碼<br/>**LPWSTR** | \- | X | X | X | \- |
| WINHTTP \_ 選項 \_ PROXY<br/>[**WINHTTP \_ PROXY \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ PROXY \_ 密碼<br/>**LPWSTR** | \- | X | X | X | \- |
| 已 \_ 使用 WINHTTP 選項 \_ PROXY \_ SPN \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ PROXY 使用者 \_ 名稱<br/>**LPWSTR** | \- | X | X | X | \- |
| WINHTTP \_ 選項 \_ 讀取 \_ 緩衝區 \_ 大小<br/>**DWORD** | \- | X | X | X | \- |
| WINHTTP \_ 選項 \_ 接收 \_ PROXY \_ CONNECT \_ 回應<br/>**BOOL** | X | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 接收 \_ 超時<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項重新 \_ 導向 \_ 原則<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 拒絕 \_ \_ URL 中的 USERPWD \_<br/>**BOOL** | \- | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 要求 \_ 優先順序<br/>**DWORD** | \- | X | X | X | \- |
| WINHTTP \_ 選項 \_ 要求 \_ 統計資料<br/>[**WINHTTP \_ 要求 \_ 統計資料**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10版本1903 |
| WINHTTP \_ 選項 \_ 要求 \_ 時間<br/>[**WINHTTP \_ 要求 \_ 時間**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10版本1903 |
| WINHTTP \_ 選項 \_ 需要 \_ STREAM \_ END<br/>**BOOL** | X | X | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ 解析 \_ 主機名稱<br/>**LPWSTR** | \- | X | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ 解析 \_ 超時<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 安全 \_ 通訊協定<br/>**DWORD** | X | \- | \- | X | \- |
| WINHTTP \_ 選項 \_ 安全性 \_ 憑證 \_ 結構<br/>[**WINHTTP \_ 憑證 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ 安全性 \_ 旗標<br/>**DWORD** | \- | X | X | X | \- |
| WINHTTP \_ 選項 \_ 安全性 \_ 資訊<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10版本2004 |
| WINHTTP \_ 選項 \_ 安全性 \_ 金鑰 \_ 位<br/>**DWORD** | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ 傳送 \_ 超時<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ 選項 \_ 伺服器 \_ CBT<br/>[**SecPkgCoNtext \_ 系結**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 鏈 \_ 內容<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10版本2004 |
| WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 內容<br/>[**憑證內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| 已 \_ 使用 WINHTTP 選項 \_ 伺服器 \_ SPN \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ SPN<br/>**DWORD** | \- | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 資料流程 \_ 錯誤碼 \_<br/>**DWORD** | \- | X | X | \- | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ TCP \_ FAST \_ 開啟<br/>**BOOL** | X | \- | \- | X | Windows 10版本2004 |
| WINHTTP \_ 選項 \_ TCP \_ KEEPALIVE<br/>[**tcp \_ keepalive**](/windows/win32/winsock/sio-keepalive-vals) | X | \- | \- | X | Windows 10版本2004 |
| WINHTTP \_ 選項 \_ TLS \_ FALSE \_ START<br/>**BOOL** | X | \- | \- | X | Windows 10版本2004 |
| WINHTTP \_ 選項 \_ TLS \_ 通訊協定不 \_ 安全 \_ 的回復<br/>**BOOL** | X | \- | \- | X | Windows 10版本21H1 |
| WINHTTP \_ 選項 \_ UNLOAD \_ 通知 \_ 事件<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| WINHTTP \_ 選項 \_ UNSAFE \_ 標頭 \_ 剖析<br/>**DWORD** | \- | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 升級 \_ 至 \_ WEB \_ 通訊端<br/>N/A | \- | X | \- | X | \- |
| WINHTTP \_ 選項 \_ URL<br/>**LPWSTR** | \- | X | X | \- | \- |
| WINHTTP \_ 選項 \_ 使用 \_ 全域 \_ 伺服器 \_ 認證<br/>**BOOL** | X | X | \- | X | \- |
| WINHTTP \_ 選項 \_ 使用者 \_ 代理程式<br/>**LPWSTR** | X | \- | X | X | \- |
| WINHTTP \_ 選項使用者 \_ 名稱<br/>**LPWSTR** | \- | X | X | X | \- |
| WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 關閉 \_ 超時<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 接收 \_ 緩衝區 \_ 大小<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 傳送 \_ 緩衝區 \_ 大小<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| WINHTTP \_ 選項背景 \_ 工作 \_ 執行緒 \_ 計數<br/>**DWORD** | \- | \- | \- | X | \- |
| WINHTTP \_ 選項 \_ 寫入 \_ 緩衝區 \_ 大小<br/>**DWORD** | \- | X | X | X | \- |

> [!Note]
> 如 Windows XP 和 Windows 2000，請參閱[執行時間需求](winhttp-start-page.md)。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|---------------------------------------------------------------------------------|
| 最低支援的用戶端 | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]            |
| 最低支援的伺服器 | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]         |
| 可轉散發套件          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。 |
| 標頭                   | WinHTTP. h                                                                       |

## <a name="see-also"></a>另請參閱

[WinHTTP 版本](winhttp-versions.md)
