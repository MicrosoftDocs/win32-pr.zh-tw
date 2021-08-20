---
description: 使用 WinHTTP 自動代理功能時，請考慮下列重要問題。
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: WinHTTP 中的自動代理問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc07ca7320fee028431ff0d89be78ee0b2dc4bb63e8191386808f0936c8a1518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052086"
---
# <a name="autoproxy-issues-in-winhttp"></a>WinHTTP 中的自動代理問題

使用 WinHTTP 自動代理功能時，請考慮下列重要問題。

## <a name="only-one-proxy-server-is-currently-supported"></a>目前只支援一部 Proxy 伺服器

WinHTTP 目前不支援指定一個以上 proxy 伺服器的 proxy 設定。 如果 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 傳回的 [**WINHTTP \_ proxy \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) 結構包含 PROXY 伺服器的清單，應用程式接著會使用 **winHTTP \_ 選項 \_ PROXY** 選項在要求控制碼上設定，winHTTP 只會使用清單中的第一部 PROXY 伺服器。 如果無法存取該 proxy 伺服器，WinHTTP 不會容錯移轉至清單中的任何其他 proxy 伺服器。 您可以使用清單中的下一個 proxy 伺服器再次設定 **WINHTTP \_ 選項 \_ PROXY** 選項，來處理這種情況的應用程式，然後再重新傳送要求。

## <a name="security-risk-mitigation"></a>安全性風險降低

處理 proxy 自動設定檔案需要執行下載的腳本程式碼。 需要考慮的一些安全性考慮：如果 PAC 檔案所在的伺服器已遭到入侵，則 PAC 腳本程式碼可能是惡意的。 因此，WinHTTP 會使用下列預防措施來保護用戶端：

1.  腳本無法將任何 ActiveX 物件具現化。 這會封鎖許多可能危險的功能，例如存取檔案和執行網路 i/o 的能力。
2.  * * Windows Server 2003： * *[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)會將整個 WPAD 處理委派給外部跨進程服務，這是在低許可權本機服務內建使用者帳戶下執行的 WinHTTP Web Proxy 自動探索服務。

3.  **Windows XP SP2 和 Windows Server 2003：** PAC 腳本的執行時間不能超過60秒，在這段時間之後，就會終止腳本執行。

4.  **Windows XP SP2 和 Windows Server 2003：** WinHTTP 會拒絕大於1MB 的 PAC 檔案。 一般 PAC 檔案的大小通常不超過數 kb。

請注意，處理 PAC 腳本的程式碼需要使用 COM，因為 WinHTTP 會使用 Microsoft JScript 元件來執行腳本。 如果 WinHTTP 無法將 WPAD 通訊協定處理委派給外部、跨進程的 Web Proxy 自動探索服務， [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 會在呼叫期間載入應用程式進程內的 COM 執行時間。 如果應用程式本身已經在使用 COM，這就不是問題所在。

## <a name="performance-considerations"></a>效能考量

自動偵測程式可能很慢，可能需要數秒鐘的時間。 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)和 [WinHttpDetectAutoProxyConfigUrl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)函數是封鎖的同步函式。 這可能是一個特定的自動偵測機制 (例如 DHCP) 比其他 (（例如 DNS) ）慢很多。 如果 **winHTTP 自動偵測 \_ \_ 型別 \_ \_ DHCP** 和 **winHTTP auto 偵測型別 \_ \_ \_ \_ DNS \_** 有指定自動偵測旗標，WINHTTP 會根據 WPAD 規格先使用 DHCP。 如果未藉由發出 DHCP 要求來探索任何 PAC URL，WinHTTP 會嘗試在已知的 DNS 位址上找出 PAC 檔案。

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 使用 WinHTTP 會話控制碼參數來快取 PAC 檔案和自動偵測的結果。 如果可能的話，最好使用相同的會話控制碼來進行多個 **WinHttpGetProxyForUrl** 呼叫，以避免重複的 PAC URL 偵測和檔案下載。 PAC 檔案只會快取在記憶體中，並在應用程式關閉會話控制碼時捨棄。

由於自動代理程式的效能影響，建議只有桌面用戶端應用程式或服務使用此功能;以伺服器為基礎的應用程式應該依賴伺服器管理員，並使用 "ProxyCfg.exe" 公用程式。

 

 



