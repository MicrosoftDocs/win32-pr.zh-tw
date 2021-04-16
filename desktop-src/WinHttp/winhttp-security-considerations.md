---
description: 下列安全性考慮適用于使用 WinHTTP 的應用程式：伺服器憑證只會在每個會話驗證一次。
ms.assetid: 287e85ed-a324-4785-872a-26e4ab37986d
title: WinHTTP 安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc06725ba03631eb4d5e5c29f8cfa0aae69b5022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469076"
---
# <a name="winhttp-security-considerations"></a>WinHTTP 安全性考慮

下列安全性考慮適用于使用 WinHTTP 的應用程式：

-   **每個會話只會驗證一次伺服器憑證。** 憑證經過驗證之後，就會在目前會話的持續時間內保持有效。 只要憑證指紋相符（指出憑證未變更），就會繼續重新驗證憑證。 因此，驗證準則中的任何變更（透過通訊協定、撤銷檢查或憑證錯誤忽略旗標）都不會在憑證驗證之後生效。 若要強制這類變更立即生效，必須先結束目前的會話，並啟動新的會話。 同樣地，只有在應用程式本身定期檢查憑證伺服器以取得到期資料時，才會偵測到會話期間的憑證到期。
-   **自動 proxy 需要下載和執行腳本。** 自動 proxy 探索支援牽涉到透過 DHCP 或 DNS 偵測、下載及執行 proxy 腳本，例如 JAVA 腳本。 若要達到更高的安全性，應用程式必須避免傳遞 WINHTTP 自動代理程式 **\_ \_ 執行執行 \_** 程式旗標，以便在跨進程起始自動 proxy 探索。 在此情況下，如果腳本無法在進程中執行，則 WinHTTP 會預設嘗試執行自動 proxy 腳本。 如果您認為此回復行為帶來無法接受的風險，請使用 WINHTTP 自動代理程式 **\_ \_ 執行 \_ \_ 僅限 OUTPROCESS** 旗標來停用回溯行為。
-   **WINHTTP \_ 狀態 \_ 回呼函數必須立即傳回。** 當您撰寫這些回呼函式的其中一個時，請小心不會封鎖。 例如，回呼或它所呼叫的任何函式都不會顯示使用者對話方塊或等候事件。 如果 [*winHTTP \_ 狀態 \_ 回檔*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 函式已封鎖，它會影響 WINHTTP 的內部排程，並導致相同進程內的其他要求被拒絕服務。
-   **WINHTTP \_ 狀態 \_ 回呼函數必須是可重新進入的。** 撰寫回呼時，請避免靜態變數或其他在 reentrance 下不安全的結構，並避免呼叫其他不可重新進入的函式。
-   **如果可以非同步作業，請針對 OUT 參數傳遞 Null。** 如果您已藉由註冊回呼函式來啟用非同步作業，請一律針對 [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)、 *lpdwBytesRead* for [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)或 *LPDWBYTESWRITTEN* for [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)，將這類 OUT 參數的 **Null** 值傳遞給 *lpdwDataAvailable* 。 在某些情況下，呼叫端執行緒會在作業完成之前終止，如果 OUT 參數不是 **Null**，則函式最後會寫入已釋放的記憶體。
-   **Passport 驗證並非萬無一失。** 任何以 cookie 為基礎的驗證配置都很容易受到攻擊。 Passport 1.4 版是以 cookie 為基礎，因此受限於與任何 cookie 或以表單為基礎的驗證配置相關的弱點。 預設會在 WinHTTP 中停用 Passport 支援;您可以使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)來啟用它。
-   **基本驗證只能透過安全連線使用。** 基本驗證會以純文字傳送使用者名稱和密碼 (請參閱 [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)) ，只能透過加密的 SSL 或 TLS 連接使用。
-   **將自動登入原則設定為「低」可能會造成風險。** 當自動登入原則設定為 [低] 時，就可以使用使用者的登入認證來對任何網站進行驗證。 不過，對不信任的網站進行驗證並不是好的安全性作法。
-   **除非明確啟用，否則不會使用 SSL 2.0 連接。** TLS 1.0 和 SSL 3.0 安全性通訊協定被視為比 SSL 2.0 更安全。 根據預設，當協調 SSL 連線（而不是 SSL 2.0）時，WinHTTP 會要求 TLS 1.0 或 SSL 3.0。 WinHTTP 中的 SSL 2.0 支援只能透過呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)來啟用。
-   **憑證-撤銷檢查必須明確要求。** 根據預設，執行憑證驗證時，WinHTTP 不會檢查伺服器的憑證是否已撤銷。 您可以使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)來啟用憑證撤銷檢查。
-   **應用程式必須確定會話對應至單一身分識別。** WinHTTP 會話應該只對應到一個身分識別;也就是說，WinHTTP 會話可用來管理單一驗證使用者或一群匿名使用者的網際網路活動。 不過，由於 WinHTTP 不會自動強制執行這項對應，因此您的應用程式必須採取步驟，以確保只涉及單一身分識別。
-   **WinHTTP 要求控制碼上的作業應進行同步處理。** 例如，應用程式應該避免在另一個執行緒正在傳送或接收要求時，在一個執行緒上關閉要求控制碼。 若要終止非同步要求，請在回呼通知期間關閉要求控制碼。 若要終止同步要求，請在上一次 WinHTTP 呼叫傳回時關閉控制碼。
-   **追蹤檔案包含機密資訊。** 追蹤檔案是使用 Access-Control 清單 (Acl 來保護) 因此通常只能由本機系統管理員或建立它的使用者帳戶來存取。避免因任何未經授權的存取而危及追蹤檔。
-   **避免透過 WinHttpSetOption 傳遞機密資料** [****](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)。 請勿提供使用者名稱、密碼或任何其他認證給 **WinHttpSetOption** ，因為您無法控制所使用的驗證配置，且機密資料可能意外地以純文字傳送。 使用 [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) 和 **WinHttpSetCredentials** ，而不是 **WinHttpSetOption** 來設定認證。
-   **自動重新導向可能會造成安全性風險。** 根據預設，重新導向 (302 訊息) 會自動遵循，即使貼文也一樣。 為了避免發生異常重新導向的可能性，應用程式應該在張貼機密資訊時，停用自動重新導向或監視回呼的重新導向。
-   **使用者定義的標頭會在重新導向之間保持不變。** 使用者定義標頭（例如以 **WinHTTPAddRequestHeaders** 新增的 cookie）會在重新導向之間傳輸，而不需要修改，而由 WinHTTP 產生的標頭會自動更新。 如果跨重新導向傳送使用者定義的標頭有安全性風險，請使用 [*winHTTP \_ 狀態 \_ 回呼*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 回呼搭配 **winHTTP \_ 回呼狀態 \_ 重新 \_ 導向** 完成，以在發生重新導向時修改問題中的標頭。
-   **WinHTTP 無法在同步模式中重新進入。** 因為 WinHTTP 無法在同步模式中重新進入，所以請勿將非同步程序呼叫排程 (APC) ，以便在執行于 WinHTTP 函式內的應用程式執行緒上呼叫 WinHTTP。 在同步模式中，WinHTTP 會執行「可提供警示等候」，如果等候中的執行緒已被先占執行 APC，之後又重新進入 WinHTTP，WinHTTP 的內部狀態可能會損毀。

 

 
