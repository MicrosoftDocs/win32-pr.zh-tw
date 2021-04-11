---
title: 核心模式快取
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021988"
---
# <a name="kernel-mode-cache"></a>核心模式快取

HTTP 伺服器版本 2.0 API 可讓應用程式以核心模式快取靜態內容的回應。 從核心快取提供要求而不轉換為使用者模式時，可以達到更高的效能。

HTTP 伺服器 API 會將適當的屬性設定套用至從核心快取提供的所有要求，包括記錄回應。 不過，需要驗證的要求將無法從快取中提供。

HTTP 伺服器 API 會將核心模式快取限制為符合下列條件的要求：

-   要求動詞命令為 GET，而且會收到整個要求。
-   要求不能有實體主體。
-   HTTP 通訊協定是1.0 版或更新版本。
-   "翻譯： f" 標頭不存在。
-   預期不會出現 "預期： 100-Continue" 以外的標頭。
-   授權標頭不存在。
-   範圍和 If-Range 的標頭不存在。

除了要求的限制之外，回應也必須符合下列條件：

-   根據預設，回應大小受限於 256 KB。 若要變更快取回應的大小，請將 **UriMaxUriBytes** 登錄值設定為所需的位元組數目。

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   您必須在 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)的單一呼叫中提供整個回應。
-   回應上的日期標頭不得隱藏。
-   如果最後修改的標頭存在，標頭的值必須具有正確的語法。 此標頭中的時間值會用於快取控制驗證。
-   核心模式快取有足夠的剩餘空間來儲存回應。

預設會啟用核心模式回應快取。 如果未符合上述要求或回應的任何條件，則會傳送回應，但不會快取。 在 HTTP 伺服器版本 2.0 API 中， [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 包含選擇性的 *pCachePolicy* 參數，可傳遞 HTTP 快取 [**\_ \_ 原則**](/windows/desktop/api/Http/ns-http-http_cache_policy) 結構。 應用程式會使用快取原則結構來設定快取。

 

 




