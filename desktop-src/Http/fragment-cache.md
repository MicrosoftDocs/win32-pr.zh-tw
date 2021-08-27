---
title: 片段快取
description: HTTP 伺服器 API 提供的功能可讓使用者將資料片段儲存在快取中，以用於快速形成 HTTP 回應。
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6659ead1139bd1b35a466a56c44357dd1f7f30cbac5fad8669445208be0e5136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047248"
---
# <a name="fragment-cache"></a>片段快取

HTTP 伺服器 API 提供的功能可讓使用者將資料片段儲存在快取中，以用於快速形成 HTTP 回應。

您可以藉由呼叫 [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) 函式，將片段新增至快取。 片段是由包含在 *pUrlPrefix* 參數中的 URL 來識別。 使用現有片段的 URL 呼叫這個函式會覆寫現有的片段。

一開始加入片段的要求佇列擁有者可以刪除或覆寫片段。 以 UrlPrefix 呼叫的 [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) 函式會刪除該前置詞內的所有片段，以及該 UrlPrefix 的階層式下階。 [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache)函式會讀取整個片段或片段內指定的位元組範圍。

> [!Note]  
> 將片段新增至快取並不保證可供未來傳送回應的呼叫使用。 片段快取專案可能會在任何時間變得無法使用。 使用無法使用之片段的呼叫會失敗。 使用片段快取的應用程式必須準備好處理此失敗。

 

## <a name="sending-a-response-with-a-fragment"></a>使用片段傳送回應

片段可以用來形成 HTTP 回應實體主體的所有或部分。 您可以藉由在 [**HTTP \_ 回應**](http-response.md)結構中指定 [**HTTP \_ 資料 \_ 區塊**](/windows/desktop/api/Http/ns-http-http_data_chunk)結構的陣列，在一個呼叫 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)函式的情況中傳送回應和實體主體。

[**HTTP \_ 資料 \_ 區塊**](/windows/desktop/api/Http/ns-http-http_data_chunk)可以指定記憶體區塊、已開啟檔案的控制碼或片段快取專案。 這些會分別對應 **至 \_ HTTP \_ 資料區塊** 類型： **HttpDataChunkFromMemory**、 **HttpDataChunkFromFileHandle** 和 **HttpDataChunkFromFragmentCache**。 HTTP 快取中的完整回應也可以做為 [**HTTP \_ 回應**](http-response.md) 結構中的片段，雖然不建議使用這種作法。

[**Http \_ 回應**](http-response.md)結構包含 [**HTTP \_ 資料 \_ 區塊**](/windows/desktop/api/Http/ns-http-http_data_chunk)結構陣列的指標，其中包含回應的實體主體。 **Http \_ 回應** 結構也包含指定 **HTTP \_ 資料 \_ 區塊** 結構陣列維度的相符計數。 **HTTP \_ 資料 \_ 區塊** 結構中的 HttpDataChunkFromFragmentCache 值會指定資料區塊的片段快取類型。 **HTTP \_ 資料 \_ 區塊** 結構也會指定片段名稱。

\_ \_ \_ 如果有任何片段快取專案無法使用，則包含快取片段的回應會失敗，並找不到錯誤路徑。 由於片段快取專案不保證可供使用，因此應用程式必須準備好處理這種情況。 處理此案例的其中一種方式是嘗試重新加入片段快取專案，然後重新傳送回應。 如果發生重複的失敗，應用程式可以使用儲存在記憶體緩衝區中的資料區塊，而不是片段快取專案。

片段快取專案也可以在 [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) 函數中指定。 這段程式碼會加入至 [**HTTP \_ 資料 \_ 區塊**](/windows/desktop/api/Http/ns-http-http_data_chunk) 結構中的實體主體，如上所述。 同樣地，如果有任何指定的片段快取專案無法使用，則傳送可能會失敗。

 

 




