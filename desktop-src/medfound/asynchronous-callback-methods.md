---
description: 非同步回呼方法
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: 非同步回呼方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967073"
---
# <a name="asynchronous-callback-methods"></a>非同步回呼方法

媒體基礎使用回呼介面提供一致的方式來執行非同步方法。

本節說明如何執行回呼介面，以及如何撰寫使用此介面的非同步方法。 其中包含下列主題。



| 主題                                                                                | 描述                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [呼叫非同步方法](calling-asynchronous-methods.md)                     | 如何在媒體基礎中呼叫非同步方法。                                               |
| [執行非同步回呼](implementing-the-asynchronous-callback.md) | 如何在 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面中執行回呼方法。 |
| [支援多個回呼](supporting-multiple-callbacks.md)                   | 如何支援相同 c + + 類別內的多個回呼。                                        |
| [工作佇列](work-queues.md)                                                       | 工作佇列可提供有效的方式，讓您在另一個執行緒上執行非同步作業。          |
| [撰寫非同步方法](writing-an-asynchronous-method.md)                 | 如何在媒體基礎中執行非同步方法。                                          |
| [自訂非同步結果物件](custom-asynchronous-result-objects.md)         | 如何提供 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的自訂執行。   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFAsyncCallback 介面**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**IMFAsyncResult 介面**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> </dl>

 

 



