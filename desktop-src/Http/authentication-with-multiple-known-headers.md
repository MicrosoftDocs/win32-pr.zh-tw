---
title: 使用多個已知標頭進行驗證
description: HTTP \_ MULTIPLE \_ 已知 \_ 標頭結構可讓伺服器應用程式將多個驗證挑戰傳送給用戶端。
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb8fd2071626d8a12f046ac0c3b6c50fcffc794462d5109a89a974f441879bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950927"
---
# <a name="authentication-with-multiple-known-headers"></a>使用多個已知標頭進行驗證

[**HTTP \_ MULTIPLE \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers)結構可讓伺服器應用程式將多個驗證挑戰傳送給用戶端。 應用程式可以透過單一驗證配置來挑戰用戶端，方法是在 [**HTTP \_ 回應**](http-response.md)所包含的 [**HTTP \_ 回應 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_response_headers)結構的 **KnownHeaders** 成員中提供 **HttpHeaderWwwAuthenticate** 列舉類型。 不過，當伺服器在使用多個驗證配置時遇到問題時，應用程式會使用 [**HTTP \_ multiple \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) 結構來提供驗證類型。

當 **HTTP \_ 回應 \_ 資訊 \_ 旗標 \_ 保留 \_ 順序** 旗標存在時，HTTP 會以指定的順序傳送驗證標頭。 如果旗標不存在，HTTP 會將驗證配置從最強到最弱排序，如下所示：

1.  交涉
2.  NTLM
3.  Digest
4.  Basic

如果驗證配置不是這些配置的其中一個，則應用程式必須指定 **HTTP \_ 回應 \_ 資訊 \_ 旗標 \_ 保留 \_ 順序旗標** 。

[**Http \_ 多個 \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers)的 **KnownHeader** 成員指向 [**HTTP \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_known_header)結構的陣列。 **HTTP \_ 已知 \_ 標頭** 結構的 **pRawValue** 成員必須指向指定配置名稱的字串。 HTTP 會剖析字串以判斷配置，並執行下列其中一個動作：

-   如果字串包含不明的驗證類型，或如果設定群組上未啟用驗證類型 () 與要求相關聯的 URL 群組或伺服器會話，HTTP 伺服器 API 會將 **pRawValue** 中的字串附加至 WWW-Authenticate 標頭。 例如，如果應用程式指定不支援的驗證配置，且 **pRawValue** 包含字串 "CustomAuthString"，則會將下列文字附加至驗證標頭：

    WWW 驗證： CustomAuthSchemeCRLF

    如果應用程式未啟用基本驗證，且 **pRawValue** 包含字串 "basic realm =" BasicRealm ""，則驗證標頭包含下列文字：

    WWW-驗證：基本領域 = "BasicRealm"

-   如果字串包含已知的驗證類型，而且存在於設定群組 (URL 群組或伺服器會話) 與要求相關聯，HTTP 伺服器 API 就會產生 WWW-Authenticate 標頭。 例如，如果在 **pRawValue** 中指定的字串為 "digest"，且在伺服器會話上啟用了 Digest，則 HTTP 伺服器 API 會將下列文字附加至驗證標頭：

    WWW-驗證：摘要領域 = " testrealm@host.com "

如果 [**HTTP \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_known_header)的 **pRawValue** 成員中的配置為 Negotiate 或 NTLM，則驗證配置名稱即已足夠。 如果指定的配置是基本的，則會將領域名稱附加至配置名稱;應用程式不需要在 **pRawValue** 中提供領域名稱。 如果指定的配置為 Digest，HTTP 會呼叫 [**AcceptSecurityCoNtext**](../SecAuthN/acceptsecuritycontext--general.md) ，以產生附加至配置名稱的挑戰。 您可以從對應的設定群組驗證資訊取得基本 (領域) 和摘要 (領域和功能變數名稱) 配置的參數。

當應用程式將多個驗證挑戰傳送至未知要求標頭中的用戶端時，HTTP 伺服器 API 會將這些挑戰傳送給用戶端，而不需要介入。 但不建議使用這種方式。

 

 




