---
title: 認證快取
description: 認證快取
ms.assetid: 6e411333-56fa-455b-a90a-f2b54f3c9545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a139d0cd90495de87f42de08687fd3157acaf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932403"
---
# <a name="credential-caching"></a>認證快取

## <a name="credential-caching-on-ntlm-ka-connections"></a>NTLM KA 連接上的認證快取

HTTP 伺服器 API 只會在 Keep-Alive (KA) 的 NTLM 驗證連接上快取認證。 根據預設，HTTP 伺服器 API 會快取在 KA 連接上傳送的第一個要求所取得的認證。 用戶端可以在不含授權標頭的 KA 連接上傳送後續要求，並根據先前建立的內容取得驗證。 在此情況下，HTTP 伺服器 API 會根據快取的認證，將權杖傳送到應用程式。 不會快取 proxy 所傳送之要求的認證。 應用程式會在對 HttpSetServerSessionProperty 或 HttpSetUrlGroupProperty 的呼叫中所提供的 [**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)結構中設定 **DisableNTLMCredentialCaching** 旗標，以停用 NTLM 認證快取。 停用認證快取時，HTTP 伺服器 API 會捨棄快取的認證，並針對每個要求執行驗證。

## <a name="ntlm-credential-caching-for-specific-urls"></a>特定 Url 的 NTLM 認證快取

應用程式會檢查 HTTP \_ 要求 \_ 驗證資訊結構的旗標參數，以判斷 HTTP 伺服器 API 傳回的要求認證是否已快取 \_ 。 此參數表示從快取 \_ \_ \_ \_ \_ \_ \_ 取出傳回的 NTLM 權杖時，快取認證的 HTTP 要求驗證旗標權杖。 認證快取是針對群組中所有 Url 的 URL 群組所指定。 不支援每個 URL 的認證快取，但應用程式可以藉由在 \_ \_ \_ \_ \_ \_ \_ HTTP \_ 要求 \_ 驗證 \_ 資訊結構中檢查快取認證旗標的 HTTP 要求驗證旗標權杖，判斷是否要在每個 url 上接受或拒絕快取的認證。 應用程式會將401驗證挑戰傳送給用戶端，以拒絕快取的認證。 用戶端接著會使用授權標頭重新傳送要求，並使用 HTTP 伺服器 API 觸發新的驗證交握。

## <a name="basic-authentication"></a>基本驗證

當要求中包含基本驗證標頭時，HTTP 伺服器 API 會剖析標頭來取得使用者名稱和密碼。 然後將使用者名稱剖析為使用者和網域部分。 HTTP 伺服器 API 會根據使用者名稱和網域金鑰，快取針對基本驗證取得的存取權杖。 收到新的要求時，HTTP 伺服器 API 會根據使用者名稱和網域抓取存取權杖。 然後，會根據快取的密碼檢查要求中的密碼。 當達到存留時間 (TTL) 限制時，就會刪除快取的存取權杖。

 

 




