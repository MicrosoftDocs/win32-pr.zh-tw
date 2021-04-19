---
description: 本主題說明 WinHTTP 5.1 版和5.0 版之間最重要的差異。
ms.assetid: df3fcf27-3012-4818-b29c-b8a4dc409828
title: WinHTTP 5.1 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909d5ae8fb1d169af01782d21d2ead56b25c940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974040"
---
# <a name="whats-new-in-winhttp-51"></a>WinHTTP 5.1 的新功能

本主題說明 WinHTTP 5.1 版和5.0 版之間最重要的差異。 其中有許多差異需要將應用程式中的程式碼變更從5.0 版遷移至5.1 版。 版本5.1 中的部分功能只有在 Windows Server 2003 和 Windows XP Service Pack 2 (SP2) 才有提供，特別是為了改善用戶端與惡意網頁伺服器的安全性有關的功能。

> [!IMPORTANT]
> 隨著 WinHTTP 5.1 版的發行，將不再提供 WinHTTP 5.0 下載。 自2004年10月1日起，Microsoft 已從 MSDN 移除 WinHTTP 5.0 SDK 下載，並已終止版本5.0 的產品支援。

 

## <a name="dll-name-change"></a>DLL 名稱變更

新的 WinHTTP 5.1 DLL 的名稱是 Winhttp.dll，而 WinHTTP 5.0 DLL 的名稱則是 Winhttp5.dll。

WinHTTP 5.0 和5.1 可並存于同一個系統;WinHTTP 5.1 不會取代或安裝 WinHTTP 5.0。

## <a name="redistribution"></a>可轉散發

WinHTTP 5.1 僅適用于 Windows Server 2003、Windows 2000 Professional Service Pack 3 (SP3) 、Windows XP 加裝 Service Pack 1 (SP1) 和更新版本的作業系統。 適用于 WinHTTP 5.1 的可轉散發合併模組 ( .msm) 檔案無法使用。

## <a name="winhttprequest-progid"></a>WinHttpRequest ProgID

WinHttpRequest 元件的 ProgID 已從 "WinHttp. WinHttpRequest. 5" 變更為 "WinHttp. WinHttpRequest. 5.1"。 [**WinHttpRequest**](winhttprequest.md)類別的 CLSID 也已變更。

## <a name="async-callback-behavior-change"></a>非同步回呼行為變更

在非同步模式中呼叫 [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)、 [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) 和 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) 函式時，請勿依賴要設定的個別 *lpdwNumberOfBytesWritten*、 *lpdwNumberOfBytesAvailable* 和 *lpdwNumberOfBytesRead* OUT 參數。 如果函式呼叫以非同步方式完成，則 WinHTTP 不會寫入應用程式程式碼所提供的這些指標。 相反地，應用程式應該使用 *lpvStatusInformation* 和 *dwStatusInformationLength* 參數將這些值取出至回呼函數。

## <a name="changes-to-default-settings"></a>預設設定的變更

預設設定的變更包括：

-   WinHTTP 5.1 中預設會啟用 SSL 伺服器憑證驗證。 當驗證伺服器憑證為嚴重錯誤時，WinHTTP 5.0 不會處理發生的失敗;系統會使用 **安全的 \_ 失敗** 回呼通知將它們回報給應用程式，但不會導致要求中止。 此外，WinHTTP 5.1 也會將伺服器憑證驗證失敗視為嚴重錯誤，以中止要求。 應用程式可以使用 **winHTTP \_ 選項 \_ 安全性 \_ 旗標** 選項，指示 WinHTTP 忽略一小部分的憑證錯誤，例如未知的 CA、無效/過期的憑證日期，或不正確憑證主體名稱。
-   WinHTTP 5.1 中預設會停用 Passport 驗證支援。 您可以使用 **WINHTTP \_ 選項 [ \_ 設定 \_ passport \_ 驗證** ] 選項來啟用 Passport 支援。 Keyring 中的自動 Passport 認證查閱預設也會停用。
-   重新導向行為變更：基於安全性理由，根據預設，HTTP 會將 url 從安全的 **HTTPs** 重新導向至一般 **HTTP：** url，因此不會再自動遵循。 有新的選項 [ **WINHTTP \_ 選項重新 \_ 導向] \_ 原則**，可覆寫 winHTTP 5.1 中的預設重新導向行為。 使用 **WinHttpRequest** COM 元件時，請使用 [新增 **WinHttpRequestOption \_ EnableHttpsToHttpRedirects** ] 選項，以啟用從 Https：到 HTTP： url 的重新導向。
-   建立 WinHTTP 追蹤檔時，存取權會受到 ACL 的限制，因此只有系統管理員可以讀取或寫入檔案。 用來建立 tracefile 的使用者帳戶也可以修改 ACL，以授與其他人存取權。 這項保護僅適用于支援安全性的檔案系統;也就是 NTFS，而非 FAT32) 。
-   從 Windows Server 2003 和 Windows XP （含 SP2）開始，將要求傳送至下列已知的非 HTTP 埠，會因為安全考慮而受到限制： 21 (FTP) 、25 (SMTP) 、70 (GOPHER) 、110 (POP3) 、119 (NNTP) 、143 (IMAP) 。
-   從 Windows Server 2003 和 Windows XP （含 SP2）開始，在 HTTP 回應中接受的標頭資料的最大數量是64K （預設值）。 如果伺服器 HTTP 回應包含更多64K 的總標頭資料，WinHTTP 將要求失敗，並出現 **錯誤 \_ WinHTTP 不正確 \_ \_ 伺服器 \_ 回應** 錯誤。 您可以使用新的 **WINHTTP \_ 選項 \_ MAX \_ RESPONSE \_ HEADER \_ SIZE** 選項來覆寫這個64k 的限制。

## <a name="ipv6-support"></a>IPv6 支援

WinHTTP 5.1 新增對網際網路通訊協定第6版 (IPv6) 的支援。 WinHTTP 可以將 HTTP 要求傳送至伺服器，其 DNS 名稱會解析成 IPv6 位址，從 Windows Server 2003 和 Windows XP SP2 開始，WinHTTP 也支援 IPv6 常值位址。

## <a name="new-options-in-the-cc-api-for-winhttp"></a>適用于 WinHTTP 的 C/c + + API 中的新選項

WinHTTP 5.1 會實行下列新選項：

<dl> 「 \# 定義 WINHTTP \_ 選項 \_ PASSPORT \_ 登出 \_ 86」  
" \# 定義 WINHTTP \_ 選項 \_ PASSPORT \_ RETURN \_ URL 87"  
「 \# 定義 WINHTTP \_ 選項重新 \_ 導向 \_ 原則88」  
</dl>

從 Windows Server 2003 和 Windows XP （含 SP2）開始，WinHTTP 5.1 會實行下列新選項。 不過，在 Windows 2000 Professional 含 SP3 或 Windows XP SP1 上，使用這些選項識別碼的 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 或 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 呼叫會失敗：

<dl> 「 \# 定義 WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時7」  
「 \# 定義 WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 自動重新 \_ 導向89」  
「 \# 定義 WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 狀態 \_ 繼續90」  
「 \# 定義 WINHTTP \_ 選項 \_ 的 \_ 回應 \_ 標頭 \_ 大小上限91」  
「 \# 定義 WINHTTP \_ 選項 \_ 最大 \_ 回應 \_ 清空 \_ 大小92」  
</dl>

## <a name="new-options-in-the-winhttprequest-51-component"></a>WinHttpRequest 5.1 元件中的新選項

WinHttpRequest 5.1 元件會執行下列新選項：

<dl> "WinHttpRequestOption \_ RevertImpersonationOverSsl"  
"WinHttpRequestOption \_ EnableHttpsToHttpRedirects"  
"WinHttpRequestOption \_ EnablePassportAuthentication"  
</dl>

從 Windows Server 2003 和 Windows XP SP2 開始，可以使用下列新的 WinHttpRequest 5.1 選項：

<dl> "WinHttpRequestOption \_ MaxAutomaticRedirects"  
"WinHttpRequestOption \_ MaxResponseHeaderSize"  
"WinHttpRequestOption \_ MaxResponseDrainSize"  
"WinHttpRequestOptions \_ EnableHttp1 \_ 1"  
</dl>

## <a name="proxies-are-not-trusted-when-auto-logon-security-is-set-to-high"></a>當自動登入安全性設定為 High 時，不信任 proxy

在 WinHTTP 5.0 中，proxy 伺服器一律受信任，可進行自動登入。 當已設定 **winHTTP 自動登入 \_ \_ 安全性 \_ 等級 \_ 高** 原則選項時，此功能不再適用于在 windows Server 2003 和 windows XP （含 SP2）上執行的 winHTTP 5.1。

## <a name="web-proxy-auto-discovery-autoproxy-api"></a>Web Proxy 自動探索 (自動代理) API

為了簡化以 WinHTTP 為基礎之應用程式的 proxy 設定，WinHTTP 現在會將 Web Proxy 自動探索 (WPAD) 通訊協定，也稱為 *自動代理程式。* 這和網頁瀏覽器（例如 Internet Explorer）的相同通訊協定會自動探索 proxy 設定，而不需要使用者手動指定 proxy 伺服器。 為了支援自動代理功能，WinHTTP 5.1 會實作為新的 C/c + + 函式、 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)，以及兩個支援的函式： [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) 和 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)。

## <a name="known-issues"></a>已知問題

下列問題已知存在於 Windows 2000 Professional SP3 和 Windows XP SP1 的 WinHTTP 5.1 中。 從 Windows Server 2003 和 Windows XP SP2 開始，WinHTTP 已解決這些問題：

-   如果應用程式在 [**WinHttpRequest**](iwinhttprequest-interface.md)元件上使用 [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)函式或 [**SetTimeouts**](iwinhttprequest-settimeouts.md)方法來設定非無限 DNS 解析超時（例如 *DwResolveTimeout* 參數），則每次 WinHTTP 解析 DNS 名稱時，就會發生執行緒控制碼流失的情況。 在大量的 HTTP 要求中，這會造成大量的記憶體流失。 因應措施是將預設的無限解析 timeout 設定維持不變 (值為0會指定無限超時) 。 在任何情況下，強烈建議您這樣做，因為 WinHTTP 中的 DNS 名稱解析的支援超時，在效能方面很昂貴。 在 Windows 2000 和更新版本中，因為基礎 DNS 用戶端服務會自行執行解析超時，所以不需要在 WinHTTP 中設定 DNS 解析超時時間。
-   處理非同步要求時，WinHTTP 不會正確處理執行緒模擬。 這會導致要求 NTLM/協商驗證的要求失敗，除非使用 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) 或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式明確指定認證。

 

 



