---
title: 'API 旗標 (Wininet. h) '
description: 許多 WinINet 函數都會接受旗標陣列作為參數。 以下是已定義旗標的簡短描述。
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966326"
---
# <a name="api-flags"></a>API 旗標

許多 WinINet 函數都會接受旗標陣列作為參數。 以下是已定義旗標的簡短描述。

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**網際網路 \_ COOKIE \_ 評估 \_ P3P**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



指出隱私權保護的平臺 (P3P) 標頭與 cookie 相關聯。


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**網際網路 \_ COOKIE \_ 第三 \_ 方**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



指出正在設定或抓取協力廠商 cookie。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**網際網路 \_ 旗標 \_ 非同步**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



只會在從這個函式傳回之控制碼的控制碼上進行非同步要求。 只有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式會使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**網際網路旗標快取 \_ \_ \_ 非同步**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



允許延遲快取寫入。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**\_ \_ \_ \_ 網路 \_ 失敗時的網際網路旗標快取**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



如果資源的網路要求因 [ \_ 網際網路連線 \_ \_ 重設錯誤](wininet-errors.md) 或 [ \_ 網際網路 \_ 無法 \_ 連線](wininet-errors.md) 錯誤而失敗，則會從快取傳回資源。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)會使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**網際網路旗標不快取 \_ \_ \_**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



不會將傳回的實體新增至快取。 這與慣用的值相同，也就是 [網際網路旗標無快取 \_ \_ \_ \_ 寫入](/windows)。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**網際網路 \_ 旗標 \_ 現有的 \_ CONNECT**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



嘗試使用現有的 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 物件（如果有的話），其屬性必須與提出要求所需的屬性相同。 這僅適用于 FTP 作業，因為 FTP 是唯一的通訊協定，通常會在同一個會話期間執行多個作業。 WinINet 會針對 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所產生的每個 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼，快取單一連接控制碼。 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)和 **InternetConnect** 函式會將此旗標用於 Http 和 Ftp 連接。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**網際網路 \_ 旗標 \_ 表單 \_ 提交**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



表示這是表單提交。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**來自快取 \_ 的網際網路旗標 \_ \_**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



不會發出網路要求。 所有實體都會從快取傳回。 如果要求的專案不在快取中， \_ \_ 則會傳回適當的錯誤，例如找不到錯誤檔案 \_ 。 只有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式會使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**網際網路 \_ 旗標 \_ FWD \_ 回**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



指出函式應使用目前在網際網路快取中的資源複本。 不會檢查資源的到期日和其他相關資訊。 如果在網際網路快取中找不到要求的專案，系統會嘗試找出網路上的資源。 此值是在 Microsoft Internet Explorer 5 中引進，並與 Internet Explorer 的 [ **向前** ] 和 [ **上一頁** ] 按鈕作業相關聯。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**網際網路 \_ 旗標 \_ 超連結**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



如果沒有過期時間，而且在決定是否要從網路重載專案時，不會從伺服器傳回任何 LastModified 時間，則會強制執行重載。 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)都可使用此旗標。

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**網際網路 \_ 旗標 \_ 忽略 \_ CERT \_ CN \_ 無效**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



停用根據要求中指定的主機名稱，從伺服器傳回的 SSL/PCT 憑證檢查。 WinINet 使用簡單的憑證檢查，方法是比較相符的主機名稱和簡單萬用字元規則。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**網際網路 \_ 旗標 \_ 忽略憑證 \_ \_ 日期 \_ 無效**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



停用 SSL/PCT 憑證的檢查，以取得適當的有效日期。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**網際網路 \_ 旗標 \_ 忽略重新 \_ 導向 \_ 至 \_ HTTP**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



停用此特殊重新導向類型的偵測。 使用這個旗標時，WinINet 會以透明的方式允許從 HTTPS 重新導向至 HTTP Url。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**網際網路 \_ 旗標 \_ 忽略重新 \_ 導向 \_ 至 \_ HTTPS**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



停用此特殊重新導向類型的偵測。 使用這個旗標時，WinINet 會以透明的方式允許從 HTTP 重新導向至 HTTPS Url。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**網際網路 \_ 旗標 \_ 保持 \_ 連接**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



針對連接使用 keep-alive 語義（如果有的話）。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (會針對 HTTP 要求) 使用此旗標。 Microsoft Network (MSN) 、NTLM 和其他類型的驗證都需要此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**網際網路 \_ 旗標 \_ 設為 \_ 持續**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



不再支援。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**網際網路 \_ 旗標必須快取 \_ \_ \_ 要求**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



與慣用值相同， **網際網路 \_ 旗標 \_ 需要 \_** 檔案。 如果無法快取檔案，則會建立暫存檔案。 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)都可使用此旗標。

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**網際網路 \_ 旗標 \_ 需要檔案 \_**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



如果無法快取檔案，則會建立暫存檔案。 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)都可使用此旗標。

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**網際網路 \_ 旗標 \_ 無 \_ 驗證**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



不會自動嘗試驗證。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**網際網路 \_ 旗標 \_ 沒有 \_ 自動重新 \_ 導向**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



不會自動處理 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)中的重新導向。 此旗標也可供 HTTP 要求的 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**網際網路 \_ 旗標無快取 \_ \_ \_ 寫入**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



不會將傳回的實體新增至快取。 、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)會使用這個旗標。

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**網際網路 \_ 旗標 \_ 無 \_ COOKIE**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



不會自動將 cookie 標頭新增至要求，也不會自動將傳回的 cookie 新增至 cookie 資料庫。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**網際網路 \_ 旗標 \_ 無 \_ UI**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



停用 cookie 對話方塊。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)只可使用此旗標 (HTTP 要求) 。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**網際網路 \_ 旗標 \_ 離線**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



與來自快取 **\_ \_ 的 \_ 網際網路旗** 標相同。 不會發出網路要求。 所有實體都會從快取傳回。 如果要求的專案不在快取中， \_ \_ 則會傳回適當的錯誤，例如找不到錯誤檔案 \_ 。 只有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式會使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**網際網路 \_ 旗標 \_ 被動式**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



使用被動 FTP 語義。 只有 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 會使用此旗標。 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 會對 ftp 要求使用此旗標，而 [**INTERNETOPENURL**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 會針對 ftp 檔案和目錄使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**網際網路 \_ 旗標 \_ PRAGMA \_ NOCACHE**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



強制源伺服器解析要求，即使 proxy 上有快取的複本也一樣。 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)函式只 (HTTP 和 HTTPS 要求) 且 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函式使用此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**網際網路 \_ 旗標 \_ 原始 \_ 資料**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



在抓取 FTP 目錄資訊時，以 [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) 結構的形式傳回資料。 如果未指定此旗標，或透過 CERN proxy 進行呼叫， [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 會傳回 HTML 版本的目錄。 只有 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函式會使用此旗標。

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：** 在抓取 Gopher 目錄資訊時，也會傳回 [**gopher \_ 尋找 \_ 資料**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) 結構。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**網際網路 \_ 旗標 \_ 讀取預先 \_ 提取**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



此旗標目前已停用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**網際網路 \_ 旗標 \_ 重載**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



強制從源伺服器下載所要求的檔案、物件或目錄清單，而不是從快取。 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)函數會使用此旗標。

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**網際網路 \_ 旗標 \_ 受限 \_ 區域**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



指出所設定的 cookie 與不受信任的網站相關聯。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**網際網路 \_ 旗標重新 \_ 同步處理**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



如果資源自上一次下載以來已經過修改，就會重載 HTTP 資源。 所有 FTP 資源都會重載。 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)都可使用此旗標。

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用，並重載 Gopher 資源。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**網際網路 \_ 旗標 \_ 安全**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



使用安全的交易語義。 這會轉譯成使用安全通訊端層/私用通訊技術 (SSL/PCT) 而且只有在 HTTP 要求中有意義。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)會使用此旗標，但如果 URL 中出現 HTTPs://，則這是多餘的。[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式會使用此旗標來進行 HTTP 連接;在此連接下建立的所有要求控制碼都會繼承此旗標。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**網際網路 \_ 旗標 \_ 轉換 \_ ASCII**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



將檔案以 ASCII 的形式傳輸 (FTP 僅) 。 此旗標可供 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)和 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**網際網路 \_ 旗標 \_ 傳輸 \_ 二進位**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



將檔案以二進位格式傳輸 (僅) 的 FTP。 此旗標可供 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)和 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**網際網路 \_ 無 \_ 回呼**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



指出該 API 不應進行任何回呼。 這會用於允許非同步作業之函式的 *dxCoNtext* 參數。


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**網際網路 \_ 選項 \_ 抑制 \_ 伺服器 \_ 驗證**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



設定 HTTP 要求物件，使其不會登入源伺服器，但會對 HTTP proxy 伺服器執行自動登入。 此選項與「要求旗標網際網路 \_ 旗標 \_ 無驗證」不同 \_ ，這會防止對 proxy 伺服器和源伺服器進行驗證。 設定此模式將會抑制使用任何認證材質 (先前提供的使用者名稱/密碼或用戶端 SSL 憑證) 在與源伺服器通訊時使用。 但是，如果要求必須透過驗證 proxy 傳輸，WinINet 仍會根據使用者的內部網路區域設定，對 HTTP proxy 執行自動驗證。 預設內部網路區域設定是允許使用使用者的預設認證進行自動登入。 為了確保隱藏所有識別資訊，呼叫端應該將 [網際網路 \_ 選項 \_ 抑制 \_ 伺服器 \_ 驗證] 與 [網際網路 \_ 旗標 \_ 無 \_ cookie 要求] 旗標合併。 此選項只能在要求物件上設定，然後才會傳送。 在傳送要求之後嘗試設定此選項，將會傳回錯誤的 \_ 網際網路 \_ 錯誤 \_ 控制碼 \_ 狀態。 此選項不需要任何緩衝區。 InternetSetOption 只會在 HttpOpenRequest 所傳回的控制碼上使用。 版本：需要 Internet Explorer 8.0 或更新版本。


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET \_ API \_ 旗標 \_ 非同步**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



強制執行非同步作業。


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**WININET \_ API \_ 旗標 \_ 同步**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



強制執行同步作業。


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WININET \_ API \_ 旗標 \_ 使用 \_ 內容**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



強制 API 使用內容值，即使它設定為零也一樣。


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



 

