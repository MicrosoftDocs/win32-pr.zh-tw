---
description: 設定錯誤記錄檔
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: 設定錯誤記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991582"
---
# <a name="setting-the-error-log"></a>設定錯誤記錄檔

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

在您執行錯誤記錄類別之後，請建立類別的新實例。 然後，藉由在時間軸上呼叫 [**IAMSetErrorLog：:p \_ 錯誤**](iamseterrorlog-put-errorlog.md)記錄檔方法，為 [DirectShow 編輯服務](directshow-editing-services.md)提供指標。 查詢 **IAMSetErrorLog** 介面的時間軸。 為確保記錄所有錯誤，您應該先呼叫這個方法，然後再載入、儲存或轉譯時間軸。


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



當您在應用程式中呼叫方法時，錯誤記錄不會影響您所收到的傳回值。 錯誤記錄會補充，但不會取代一般的錯誤處理技巧。 若要建立健全的應用程式，請一律檢查 HRESULT 值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[記錄錯誤](logging-errors.md)
</dt> </dl>

 

 



