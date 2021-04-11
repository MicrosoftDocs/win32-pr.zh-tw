---
title: '驗證 (HTTP 伺服器 API) '
description: 從2.0 版開始，HTTP 伺服器 API 會執行應用程式的伺服器端驗證。
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d523df90861c83a45f67811edad243ceee5165
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383642"
---
# <a name="authentication-http-server-api"></a>驗證 (HTTP 伺服器 API) 

某些伺服器應用程式需要用戶端驗證才能存取資源和服務 HTTP 要求。 從2.0 版開始，HTTP 伺服器 API 會執行應用程式的伺服器端驗證。 在 HTTP 伺服器 API 版本1.0 中，伺服器應用程式必須執行自己的驗證。 HTTP 伺服器 API 執行驗證的一些優點包括：

-   應用程式可在低許可權下執行，進而降低安全性風險。
-   驗證會以核心模式執行，因此會在驗證期間減少從使用者模式到核心模式的轉換。
-   在核心模式中執行的驗證可讓伺服器應用程式在不同的使用者帳戶上執行。 在1.0 版中，電腦上的所有應用程式都必須在相同的使用者帳戶下執行，以在服務主體名稱 (SPN) 進行驗證。
-   如果在交握過程中回收工作者進程，就不會重設 NTLM 驗證交握。

為了充分利用2.0 版驗證，應用程式會啟用 HTTP 伺服器 API 套用至應用程式已註冊之 Url 的驗證配置。 可以在伺服器會話或 URL 群組上啟用驗證。 如果未在 URL 群組上設定，則 URL 群組會繼承伺服器會話所啟用的驗證配置。 HTTP 伺服器 API 支援下列配置：

-   交涉
-   NTLM
-   Digest
-   基本

伺服器應用程式也可以執行 HTTP 伺服器 API 不支援的驗證配置。 HTTP 伺服器 API 會將要求傳送至應用程式，以取得不支援的驗證配置，或應用程式尚未啟用的配置。

### <a name="enabling-authentication"></a>啟用驗證

伺服器應用程式會使用 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) 或 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) 函數，在伺服器會話或 URL 群組上啟用及設定驗證，如下所示：

1.  應用程式會在 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)或 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)的 *Property* 參數中指定 **HttpServerAuthenticationProperty** ，以啟用驗證。
2.  應用程式會在 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)或 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)的 *PPropertyInformation* 參數中，指定 [**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)結構中的設定參數。 應用程式會指定啟用的驗證配置、是否停用 NTLM 認證快取，並在 **HTTP \_ 伺服器 \_ 驗證 \_ 資訊** 結構中提供基本和摘要參數。

### <a name="authentication-procedure"></a>驗證程式

若要起始 HTTP 伺服器驗證，應用程式會在第一個要求抵達要求佇列之前啟用驗證屬性。 下列步驟是驗證要求的一般處理流程。

1.  應用程式會啟用驗證。 請參閱前面的「啟用驗證」一節。
    > [!Note]  
    > 用戶端傳送未經驗證的要求。 HTTP 伺服器 API 會將要求傳遞至伺服器應用程式，並讓它產生最初的401挑戰。 HTTP 伺服器 API 包含內嵌于 [**HTTP \_ 要求**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))結構的 [**HTTP \_ 要求 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_request_auth_info)結構。 **AuthStatus** 成員指出 **HttpAuthStatusNotAuthenticated**

     

2.  應用程式會檢查 [**HTTP \_ 要求 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_request_auth_info)結構的 **AuthStatus** 成員，以判斷要求是否經過驗證。 如果要求尚未經過驗證，應用程式可以將要求以匿名方式服務，或傳送最初的401驗證挑戰。
3.  如果應用程式將要求以匿名方式服務，則它會處理要求，並將最終回應傳送給用戶端應用程式，就像驗證未涉及一樣。
4.  如果應用程式需要驗證，它會傳送一或多個 WWW-Authenticate 標頭給用戶端的可用配置，以傳送初始401挑戰。 當回應中傳送一個以上的驗證標頭時，應用程式應該使用 [**HTTP \_ MULTIPLE \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) 結構來建立必要的標頭集合。
    > [!Note]
    >
    > 用戶端會使用從伺服器應用程式所指定的一組可用配置的授權標頭，重新傳送要求給初始401回應中所指定的架構。
    >
    > HTTP 伺服器 API 會檢查授權要求授權標頭，以判斷是否已啟用此配置。 如果是，則 HTTP 伺服器 API 會執行驗證，並處理所有過渡要求/401-回應交換，直到驗證交握完成為止。
    >
    > 當 HTTP 伺服器 API 完成驗證嘗試時，它會將要求傳送至應用程式，並在要求所傳回的 [**HTTP \_ 要求 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_request_auth_info) 結構中嘗試驗證的結果。 如果驗證嘗試因下列其中一個原因而失敗，HTTP 伺服器 API 不會將要求傳遞至應用程式：
    >
    > -   如果驗證交握因為內部 HTTP 伺服器 API 錯誤（例如記憶體配置失敗）而失敗，則 HTTP 伺服器 API 會產生 503 (服務無法使用) 回應，並傳回給用戶端。
    > -   如果有格式不正確的授權標頭，例如沒有配置名稱的標頭，或遇到格式不正確的用戶端認證 Base64 編碼，則 HTTP 伺服器 API 會產生 400 (錯誤的) 要求，並傳回給用戶端。

     

5.  伺服器應用程式會檢查 [**HTTP \_ 要求 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_request_auth_info)結構的 **AuthStatus** 成員，以判斷驗證是否成功。 當驗證失敗時，HTTP 伺服器 API 會在 **HTTP \_ 要求 \_ 驗證 \_ 資訊** 結構的 **SecStatus** 成員中包含從 [AcceptSecurityCoNtext](/previous-versions/windows/embedded/ms937012(v=msdn.10))傳回的錯誤。 如果驗證嘗試因為認證不正確而失敗，應用程式可能會產生另一個具有所需 WWW-Authenticate 標頭的401挑戰，或可能決定以匿名方式提供要求的服務。
6.  如果驗證成功，應用程式會使用 [**HTTP \_ 要求 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_request_auth_info) 結構中提供的權杖來模擬用戶端及存取資源。 只要要求識別碼有效，這通常會在應用程式完成要求的回應之前，傳回給應用程式的存取權杖控制碼有效。 不過，權杖可能會在這段期間過期，而應用程式可能需要將另一個401挑戰傳送給用戶端。
7.  應用程式會傳送最終的200正常回應，而且必須關閉存取權杖的控制碼。
    > [!Note]  
    > HTTP 伺服器 API 會將相互驗證資料附加至最終的 200 OK 回應（如果在驗證交握期間產生的話）。

     

### <a name="ntlm-null-sessions"></a>NTLM Null 會話

請注意，在最終安全性內容中指出的 NTLM Null 會話不會被視為已驗證。 在此情況下，會將要求傳送至應用程式，並在 [**HTTP \_ 要求 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_request_auth_info) 結構中出現 HttpAuthStatusFailure 錯誤，而應用程式可能會傳送另一個401挑戰。

### <a name="preemptive-authentication"></a>搶先驗證

根據 HTTP 通訊協定，在用戶端建立資源的驗證之後，它可以事先將對應的授權標頭與後續的資源連續要求一起傳送，而不需要等待伺服器的401挑戰。 如果應用程式仍啟用授權標頭中所指出的配置，而且 HTTP 伺服器 API 支援此配置，則 HTTP 伺服器會嘗試驗證，而不會將要求傳送至應用程式。 當應用程式收到這類型的驗證要求時，可以選擇捨棄要求並重新產生初始401挑戰，或將要求服務為已驗證的要求。

### <a name="mutual-authentication"></a>相互驗證

在交握期間使用協商配置時，會產生相互驗證資料，並將其解析為 Kerberos，並要求用戶端進行相互驗證。 HTTP 伺服器 API 會在伺服器應用程式傳送的最終200正常回應中自動插入相互驗證資料。 根據預設，HTTP 伺服器 API 不會將相互驗證資料傳遞到伺服器應用程式，因為它會自動處理它的傳送。 但是，如果伺服器應用程式在設定的 [**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)結構中啟用了 ReceiveMutualAuth 旗標，則會將相互驗證資料傳遞給以已驗證的 [**HTTP \_ 要求**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))內嵌的 [**HTTP \_ 要求 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_request_auth_info)結構中的應用程式。 在此情況下，應用程式應該傳送具有最終200正常回應的相互驗證資料。 在單一電腦提供多個網站的情況下，電腦上的所有網站都會使用網域中本機電腦帳戶的認證來進行相互驗證。

 

 
