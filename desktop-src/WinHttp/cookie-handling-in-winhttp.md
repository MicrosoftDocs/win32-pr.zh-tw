---
description: WinHTTP 中的 Cookie 處理
ms.assetid: ef0f0847-05f6-4477-8e48-e0bea66314ab
title: WinHTTP 中的 Cookie 處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b596225dc3c741ab9ed0139a63e343e7afb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998009"
---
# <a name="cookie-handling-in-winhttp"></a>WinHTTP 中的 Cookie 處理

在要求或回應的 cookie 標頭中，用戶端和伺服器之間傳遞 HTTP 會話資料。 伺服器會將 cookie 傳送至回應的設定 cookie 標頭中的用戶端，而 WinHTTP API 會在要求的 cookie 標頭中，將伺服器 cookie 重新傳送至伺服器。  (HTTP 狀態管理機制) 2109 中所述的 cookie 處理規格，預設會在 WinHTTP 中執行。 WinHTTP 不支援最新的 cookie 處理規格（于 rfc 2964 中所述）。

WinHTTP 會從伺服器 Set-Cookie 標頭取得 cookie，並根據每個會話將其儲存在快取中。 在與 cookie 來源相符之相同 WinHTTP 會話中的後續要求上，會重新傳送此 cookie。 WinHTTP API 會重新產生要求中每個階段的要求 cookie 標頭。

下列清單說明 WinHTTP 用戶端應用程式可用來處理 cookie 的數個選項：

-   自動處理 Cookie-WinHTTP 會自動處理 cookie，而用戶端應用程式不會執行任何自訂的 cookie 處理。
-   停用自動 Cookie 處理-WinHTTP API 中的自動 cookie 處理已停用，且未傳送任何 cookie。
-   手動指定所有 Cookie –自動 cookie 處理已停用，而且用戶端應用程式會針對會話中的每個要求新增或移除所有 cookie 標頭。
-   手動和自動 Cookie 處理-結合自動和手動 cookie 處理。

## <a name="disabling-automatic-cookie-handling"></a>停用自動 Cookie 處理

為了停用 cookie 處理，WinHTTP 用戶端應用程式會呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式，並將 *dwOption* 參數設定為 winHTTP \_ OPTION \_ disable \_ 功能，並將 *lpBuffer* 參數設定為 winHTTP \_ 停用 \_ cookie。 *HInternet* 參數可以是會話控制碼或要求控制碼。 在傳送前一個要求的要求控制碼上停用 cookie 處理時，用戶端應該先以 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) 函式手動移除現有的要求 cookie 標頭，然後再傳送下一個要求。 如需詳細資訊，請參閱 [移除 Cookie 標頭](#removing-cookie-headers)。

**注意**  用戶端應用程式必須在停用自動模式之後，設定會話的所有 cookie。

## <a name="manually-specifying-all-cookies"></a>手動指定所有 Cookie

停用自動 cookie 處理時，WinHTTP 用戶端應用程式可以選擇手動指定所有 cookie。 為了手動設定 cookie，應用程式會呼叫 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) ，在 *pwszHeaders* 參數中指定 cookie 標頭。 用戶端應用程式應該先清除所有 cookie 標頭，然後再重新傳送要求。

用戶端應用程式也應該在重新導向要求時變更 cookie 標頭。 若要在重新導向的要求上變更 cookie，用戶端會以回應重新導向回呼案例的 [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) 來指定回呼函式。 回呼處理常式應該會藉由呼叫 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)來清除先前在要求上傳送的 cookie。 如需移除 cookie 標頭的詳細資訊，請參閱 [移除 Cookie 標頭](#removing-cookie-headers)。

## <a name="manual-and-automatic-cookie-handling"></a>手動和自動 Cookie 處理

WinHTTP 用戶端應用程式可以結合 WinHTTP 自動 cookie 處理機制與手動的 cookie 處理。 應用程式會先將自訂 cookie 新增至自動產生的 cookie 標頭，然後再使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 函式傳送要求。 自訂 cookie 應為 WinHTTP API 要求中的第一個 cookie 標頭，才能正確地快取 cookie。 用戶端應用程式也應該移除先前要求所傳送的 cookie，然後再重新傳送相同要求控制碼上的要求。 如需詳細資訊，請參閱移除 Cookie 標頭。

在呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 之前新增至要求的 cookie 會包含在代表下一個 **WinHttpSendRequest** 和 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 呼叫傳送的所有 WinHTTP 要求中。 用戶端應用程式可能需要在重新導向要求時清除 cookie 標頭。 為了在重新導向的要求上清除 cookie，用戶端會以回應重新導向回呼案例的 [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) 來指定回呼函數。 回呼處理常式應藉由呼叫 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)來清除先前在要求上傳送的 cookie。 回呼函式可能不會在重新導向回呼上設定新的自訂 cookie。 用戶端必須等待 **WinHttpReceiveResponse** 完成，才能為下一個 **WinHttpSendRequest** 呼叫新增 cookie。

## <a name="removing-cookie-headers"></a>移除 Cookie 標頭

在重新傳送要求之前，WinHTTP 用戶端應用程式可能需要清除現有的要求 cookie，以防止先前要求上傳送的 cookie 在目前的要求上再次傳送;如需詳細資訊，請參閱下列注意事項。 另外也請注意，在要求控制碼上傳送第一個要求之前，不需要清除 Cookie。 用戶端可以藉由呼叫 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) 和 *pwszHeaders* 參數中的空白 cookie 標頭，以及在 \_ \_ \_ *dwModifier* 參數中設定的 WINHTTP ADDREQ 旗標取代旗標，來清除現有的 cookie。 下列程式碼範例顯示如何清除要求上的 cookie 標頭。

``` syntax
WinHttpAddRequestHeaders( hRequest, 
                          L"Cookie:", 
                          -1, 
                          WINHTTP_ADDREQ_FLAG_REPLACE);
```

針對 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 Service Pack 1 (SP1) 之前的作業系統版本，WinHTTP API 具有不同的 cookie 處理行為。

* * Windows XP SP2 和更新版本，以及 Windows Server 2003 SP1 和更新版本： * *

WinHTTP API 會清除針對要求控制碼在先前要求上傳送的所有 cookie。 用戶端可以在每次呼叫 WinHttpSendRequest 之前，手動新增 cookie 標頭。 如果未停用 WinHTTP API 的自動 cookie 處理功能，WinHTTP API 將會附加新的 cookie 標頭 (或加入新的 cookie 標頭，如果用戶端應用程式沒有以手動方式) 與伺服器上的 cookie 一併加入新的 cookie 標頭。

* * Windows XP 加裝 SP2 和 Windows Server 2003 SP1： * *

在 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 完成之後，WinHTTP API 不會清除要求 cookie 標頭。 在先前的要求中傳送的 cookie 將會在後續的 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)呼叫中重新傳送。 WinHTTP 用戶端應用程式應該先清除現有的 cookie 標頭，然後再重新傳送要求控制碼上的要求。

 

 



